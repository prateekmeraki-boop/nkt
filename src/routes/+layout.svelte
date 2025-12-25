<script>
  import '../app.css';
  import FloatingIcon from '$lib/icons/FloatingIcons.svelte';
  import LoadingBar from '$lib/components/LoadingBar.svelte';
  import { page } from '$app/stores';
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';  // ← ADD THIS
  
  let mobileMenuOpen = false;
  let mounted = false;
  
  // Close mobile menu when navigating to a new page
  $: if ($page.url.pathname) {
    mobileMenuOpen = false;
  }
  
  onMount(() => {
    // Register service worker
    if ('serviceWorker' in navigator) {
      navigator.serviceWorker.register('/sw.js')
        .then(registration => {
          console.log('SW registered:', registration);
        })
        .catch(error => {
          console.log('SW registration failed:', error);
        });
    }
  });
  
  // Close menu when clicking outside
  function handleClickOutside(event) {
    if (mobileMenuOpen && !event.target.closest('.mobile-menu-container')) {
      mobileMenuOpen = false;
    }
  }

  // Toggle body class for scroll lock
  $: {
    if (typeof document !== 'undefined') {
      if (mobileMenuOpen) {
        document.body.classList.add('menu-open');
      } else {
        document.body.classList.remove('menu-open');
      }
    }
  }
</script>

<svelte:window on:click={handleClickOutside} />

<!-- Skip to main content link (for screen readers and keyboard users) -->
<a 
  href="#main-content" 
  class="sr-only focus:not-sr-only focus:absolute focus:top-4 focus:left-4 focus:z-[200] focus:px-6 focus:py-3 focus:bg-[#ED7D31] focus:text-white focus:rounded-lg focus:shadow-lg"
>
  Skip to main content
</a>

<svelte:head>
  <title>NK Technologies</title>
  <meta name="description" content="NK Technologies - Technological Solutions Company based in Pune, Maharashtra." />
</svelte:head>

<!-- Add this right after the opening tag -->
<LoadingBar />

<!-- Header/Navigation -->
<header class="fixed top-0 left-0 right-0 z-50 bg-[#100A40]/90 backdrop-blur-md border-b border-white/10">
  <nav class="container mx-auto px-6 py-4">
    <div class="flex items-center justify-between">
      <!-- Logo -->
      <a href="/" class="flex items-center gap-2 text-white font-bold text-xl">
        <img 
          src="/logo.svg" 
          alt="NK Technologies Logo" 
          class="h-8 w-8"
        />
        <span class="hidden sm:inline">NK TECHNOLOGIES</span>
        <span class="sm:hidden">NK TECH</span>
      </a>
      
      <!-- Desktop Navigation -->
<!-- Desktop Navigation -->
<div class="hidden md:flex items-center gap-6">
  <a 
    href="/"
    class="transition-colors px-4 py-2 rounded-lg font-medium
           {$page.url.pathname === '/' 
             ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
             : 'text-white hover:text-[#ED7D31]'}"
    aria-current={$page.url.pathname === '/' ? 'page' : undefined}
  >
    Home
  </a>
  <a 
    href="/about"
    class="transition-colors px-4 py-2 rounded-lg font-medium
           {$page.url.pathname === '/about' 
             ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
             : 'text-white hover:text-[#ED7D31]'}"
    aria-current={$page.url.pathname === '/about' ? 'page' : undefined}
  >
    About
  </a>
  <a 
    href="/services"
    class="transition-colors px-4 py-2 rounded-lg font-medium
           {$page.url.pathname === '/services' 
             ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
             : 'text-white hover:text-[#ED7D31]'}"
    aria-current={$page.url.pathname === '/services' ? 'page' : undefined}
  >
    Services
  </a>
  <a 
    href="/contact"
    class="transition-colors px-4 py-2 rounded-lg font-medium
           {$page.url.pathname === '/contact' 
             ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
             : 'text-white hover:text-[#ED7D31]'}"
    aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}
  >
    Contact
  </a>
        
<a 
  href="tel:+919730553516"
  class="relative px-6 py-2 font-semibold rounded-lg overflow-hidden group
         bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]
         hover:shadow-lg hover:shadow-cyan-300/50 transition-all duration-300
         transform hover:scale-105 animate-pulse-gentle"
>
  <!-- Animated gradient overlay on hover (reverse direction) -->
  <span class="absolute inset-0 bg-gradient-to-r from-[rgb(255,229,243)] to-[rgb(222,255,252)] opacity-0 group-hover:opacity-100 transition-opacity duration-300"></span>
  
  <!-- Button text -->
  <span class="relative z-10 flex items-center gap-2">
    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
    </svg>
    Call Now
  </span>
  
  <!-- Shimmer effect -->
  <span class="absolute inset-0 -translate-x-full group-hover:translate-x-full transition-transform duration-1000 bg-gradient-to-r from-transparent via-white/30 to-transparent"></span>
</a>


      </div>
      
      <!-- Mobile Menu Button -->
      <button 
        class="md:hidden text-white p-2 hover:bg-white/10 rounded-lg transition-colors mobile-menu-container"
        on:click={() => mobileMenuOpen = !mobileMenuOpen}
        aria-label="Toggle mobile menu"
        aria-expanded={mobileMenuOpen}
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          {#if !mobileMenuOpen}
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
          {:else}
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
          {/if}
        </svg>
      </button>
    </div>
    
    <!-- Mobile Menu Dropdown -->
{#if mobileMenuOpen}
  <div class="md:hidden mt-4 pb-4 border-t border-white/10 pt-4 mobile-menu-container animate-slide-down">
    <div class="flex flex-col space-y-3">
      <a 
        href="/"
        class="transition-all px-4 py-3 rounded-lg font-medium
               {$page.url.pathname === '/' 
                 ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
                 : 'text-white hover:text-[#ED7D31] hover:bg-white/5'}"
      >
        Home
      </a>
      <a 
        href="/about"
        class="transition-all px-4 py-3 rounded-lg font-medium
               {$page.url.pathname === '/about' 
                 ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
                 : 'text-white hover:text-[#ED7D31] hover:bg-white/5'}"
      >
        About
      </a>
      <a 
        href="/services"
        class="transition-all px-4 py-3 rounded-lg font-medium
               {$page.url.pathname === '/services' 
                 ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
                 : 'text-white hover:text-[#ED7D31] hover:bg-white/5'}"
      >
        Services
      </a>
      <a 
        href="/contact"
        class="transition-all px-4 py-3 rounded-lg font-medium
               {$page.url.pathname === '/contact' 
                 ? 'bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40]' 
                 : 'text-white hover:text-[#ED7D31] hover:bg-white/5'}"
      >
        Contact
      </a>
      

<a 
  href="tel:+919730553516"
  class="relative px-6 py-3 font-semibold rounded-lg overflow-hidden group
         bg-gradient-to-r from-[rgb(222,255,252)] to-[rgb(255,229,243)] text-[#100A40] text-center
         hover:shadow-lg hover:shadow-cyan-300/50 transition-all duration-300
         animate-pulse-gentle"
>
  <span class="absolute inset-0 bg-gradient-to-r from-[rgb(255,229,243)] to-[rgb(222,255,252)] opacity-0 group-hover:opacity-100 transition-opacity duration-300"></span>
  
  <span class="relative z-10 flex items-center justify-center gap-2">
    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
    </svg>
    Call Now
  </span>
  
  <span class="absolute inset-0 -translate-x-full group-hover:translate-x-full transition-transform duration-1000 bg-gradient-to-r from-transparent via-white/30 to-transparent"></span>
</a>


        </div>
      </div>
    {/if}
  </nav>
</header>

<!-- Main Content -->
<div class="min-h-screen flex flex-col bg-[#100A40] text-white">
  <main id="main-content" class="flex-1 pt-16" tabindex="-1">  <!-- Add id and tabindex -->
    {#key $page.url.pathname}
      <div in:fade={{ duration: 300, delay: 300 }} out:fade={{ duration: 300 }}>
        <slot />
      </div>
    {/key}
  </main>
  
  <footer class="border-t border-white/10 py-8">
    <div class="container mx-auto px-6">
      <p class="text-center text-gray-400 text-sm">
        © {new Date().getFullYear()} NK Technologies. All rights reserved.
      </p>
    </div>
  </footer>
</div>

<!-- Floating Buttons -->
<div class="fixed left-4 bottom-4 flex flex-col gap-3 z-30">
  <!-- Call -->
  <a href="tel:+919730553516" aria-label="Call Us">
    <FloatingIcon label="Call Us">
      <svg xmlns="http://www.w3.org/2000/svg"
           viewBox="0 0 24 24"
           class="h-5 w-5 text-white">
        <path fill="currentColor"
          d="M6.62 10.79a15.46 15.46 0 0 0 6.59 6.59l2.2-2.2a1 1 0 0 1 .96-.26
             11.36 11.36 0 0 0 3.56.57 1 1 0 0 1 1 1V20a1 1 0 0 1-1 1A17 17 0 0 1 3 4
             a1 1 0 0 1 1-1h3.5a1 1 0 0 1 1 1 11.36 11.36 0 0 0 .57 3.56 1 1 0 0 1-.26.96z"/>
      </svg>
    </FloatingIcon>
  </a>

  <!-- Home -->
  <a href="/" aria-label="Home">
    <FloatingIcon label="Home">
      <svg xmlns="http://www.w3.org/2000/svg"
           viewBox="0 0 24 24"
           class="h-5 w-5 text-white">
        <path fill="currentColor"
          d="M12 3 3 10h2v10h6v-6h2v6h6V10h2z"/>
      </svg>
    </FloatingIcon>
  </a>

  <!-- Contact -->
  <a href="/contact" aria-label="Contact">
    <FloatingIcon label="Contact">
      <svg xmlns="http://www.w3.org/2000/svg"
           viewBox="0 0 24 24"
           class="h-5 w-5 text-white">
        <path fill="currentColor"
          d="M4 4h16a1 1 0 0 1 1 1v14l-4-3H4a1 1 0 0 1-1-1V5a1 1 0 0 1 1-1zm1 2v9h11.2L19 16.8V6z"/>
      </svg>
    </FloatingIcon>
  </a>
</div>

<style>
  @keyframes slide-down {
    from {
      opacity: 0;
      transform: translateY(-10px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .animate-slide-down {
    animation: slide-down 0.3s ease-out;
  }
  
  /* Prevent body scroll when mobile menu is open */
  :global(body.menu-open) {
    overflow: hidden;
  }

  /* Gentle pulsing animation */
  @keyframes pulse-gentle {
    0%, 100% {
      opacity: 1;
      transform: scale(1);
    }
    50% {
      opacity: 0.95;
      transform: scale(1.02);
    }
  }
  
  .animate-pulse-gentle {
    animation: pulse-gentle 2s ease-in-out infinite;
  }
  
  /* Stop pulsing on hover */
  .animate-pulse-gentle:hover {
    animation: none;
  }

  @keyframes slide-down {
    from {
      opacity: 0;
      transform: translateY(-10px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .animate-slide-down {
    animation: slide-down 0.3s ease-out;
  }
  
  /* Prevent body scroll when mobile menu is open */
  :global(body.menu-open) {
    overflow: hidden;
  }
</style>
