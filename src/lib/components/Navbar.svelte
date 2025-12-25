<script lang="ts">
  import { page } from '$app/stores';
  let mobileMenuOpen = false;

  const links = [
    { href: '/', label: 'Home' },
    { href: '/about', label: 'About' },
    { href: '/services', label: 'Services' },
    { href: '/contact', label: 'Contact' }
  ];

  const toggleMenu = () => {
    mobileMenuOpen = !mobileMenuOpen;
  };
</script>

<nav class="sticky top-0 z-40 glass border-b border-nk-border">
  <div class="mx-auto max-w-7xl flex items-center justify-between px-4 sm:px-6 py-3 md:py-4">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-3 flex-shrink-0 hover:opacity-80 transition">
      <svg
        width="40"
        height="40"
        viewBox="0 0 882 882"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <defs>
          <linearGradient id="nk-gradient" x1="0" y1="0" x2="1" y2="0">
            <stop offset="0" style="stop-color:rgb(222,255,252);stop-opacity:1" />
            <stop offset="1" style="stop-color:rgb(255,229,243);stop-opacity:1" />
          </linearGradient>
        </defs>
        <g transform="matrix(2.19281e-16,3.58115,-3.58113,2.19282e-16,723.073,-848.202)">
          <path
            d="M421.704,66.48L483.141,152.491L364.505,152.491L364.505,5.043L483.141,5.043L421.704,66.48ZM416.196,71.988L372.343,115.841L372.343,144.653L468.1,144.653L416.196,71.988Z"
            style="fill:url(#nk-gradient);fill-rule:nonzero;"
          />
        </g>
        <g transform="matrix(2.19281e-16,-3.58115,3.58113,2.19282e-16,159.679,1723.38)">
          <path
            d="M362.174,152.279L362.174,4.831L370.437,4.831L473.396,105.037L473.396,4.831L481.235,4.831L481.235,152.279L362.174,152.279Z"
            style="fill:url(#nk-gradient);fill-rule:nonzero;"
          />
        </g>
      </svg>

      <span class="hidden sm:inline font-bold tracking-tight text-white">
        NK TECHNOLOGIES
      </span>
    </a>

    <!-- Desktop Nav -->
    <div class="hidden md:flex items-center gap-1">
      {#each links as link}
        <a
          href={link.href}
          class="px-3 py-1.5 rounded-lg text-sm font-medium transition
            {$page.url.pathname === link.href
            ? 'bg-nk-accent text-slate-950'
            : 'text-slate-300 hover:text-nk-accent hover:bg-white/5'}"
        >
          {link.label}
        </a>
      {/each}
    </div>

    <!-- Desktop CTA Button with Pulsing Animation -->
    <a 
      href="tel:+919730553516"
      class="hidden md:block relative px-6 py-2 font-semibold rounded-lg overflow-hidden group
             bg-gradient-to-r from-[#ED7D31] to-orange-600 text-[#100A40]
             hover:shadow-lg hover:shadow-[#ED7D31]/50 transition-all duration-300
             transform hover:scale-105 animate-pulse-gentle"
    >
      <!-- Animated gradient overlay on hover -->
      <span class="absolute inset-0 bg-gradient-to-r from-orange-600 to-[#ED7D31] opacity-0 group-hover:opacity-100 transition-opacity duration-300"></span>
      
      <!-- Button text -->
      <span class="relative z-10 flex items-center gap-2">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
        </svg>
        Call Now
      </span>
      
      <!-- Shimmer effect -->
      <span class="absolute inset-0 -translate-x-full group-hover:translate-x-full transition-transform duration-1000 bg-gradient-to-r from-transparent via-white/20 to-transparent"></span>
    </a>

    <!-- Mobile Menu Toggle -->
    <button
      class="md:hidden p-2 rounded-lg hover:bg-white/5 transition text-white"
      on:click={toggleMenu}
      aria-label="Toggle menu"
    >
      {#if mobileMenuOpen}
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
        </svg>
      {:else}
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      {/if}
    </button>
  </div>

  <!-- Mobile Menu Dropdown -->
  {#if mobileMenuOpen}
    <div class="md:hidden px-4 pb-4 border-t border-white/10 pt-4 animate-slide-down">
      <div class="flex flex-col space-y-3">
        {#each links as link}
          <a
            href={link.href}
            class="text-white hover:text-[#ED7D31] hover:bg-white/5 transition-all px-4 py-3 rounded-lg
              {$page.url.pathname === link.href ? 'bg-[#ED7D31] text-white' : ''}"
            on:click={() => mobileMenuOpen = false}
          >
            {link.label}
          </a>
        {/each}
        
        <!-- Enhanced Mobile Call Now Button -->
        <a 
          href="tel:+919730553516"
          class="relative px-6 py-3 font-semibold rounded-lg overflow-hidden group
                 bg-gradient-to-r from-[#ED7D31] to-orange-600 text-[#100A40] text-center
                 hover:shadow-lg hover:shadow-[#ED7D31]/50 transition-all duration-300
                 animate-pulse-gentle"
        >
          <span class="absolute inset-0 bg-gradient-to-r from-orange-600 to-[#ED7D31] opacity-0 group-hover:opacity-100 transition-opacity duration-300"></span>
          
          <span class="relative z-10 flex items-center justify-center gap-2">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
            </svg>
            Call Now
          </span>
          
          <span class="absolute inset-0 -translate-x-full group-hover:translate-x-full transition-transform duration-1000 bg-gradient-to-r from-transparent via-white/20 to-transparent"></span>
        </a>
      </div>
    </div>
  {/if}
</nav>

<style>
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

  /* Slide down animation for mobile menu */
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
</style>
