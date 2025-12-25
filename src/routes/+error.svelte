<script>
  import { page } from '$app/stores';
  import SEO from '$lib/components/SEO.svelte';
  
  // Get error details
  $: status = $page.status;
  $: errorMessage = $page.error?.message || 'Something went wrong';
  
  // Different messages for different error codes
  const errorMessages = {
    404: {
      title: 'Page Not Found',
      description: 'Sorry, we couldn\'t find the page you\'re looking for.',
      suggestion: 'The page might have been moved or deleted.'
    },
    500: {
      title: 'Server Error',
      description: 'Oops! Something went wrong on our end.',
      suggestion: 'Please try again later or contact us if the problem persists.'
    },
    403: {
      title: 'Access Denied',
      description: 'You don\'t have permission to access this page.',
      suggestion: 'Please contact us if you believe this is a mistake.'
    }
  };
  
  $: currentError = errorMessages[status] || {
    title: 'Error',
    description: errorMessage,
    suggestion: 'Please try again or return to the homepage.'
  };
   let konami = [];
  const konamiCode = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'b', 'a'];
  
  function handleKeydown(event) {
    konami.push(event.key);
    konami = konami.slice(-10);
    
    if (konami.join(',') === konamiCode.join(',')) {
      alert('🎉 You found the secret! But this page is still 404 😅');
    }
  }
</script>

<svelte:window on:keydown={handleKeydown} />

<SEO 
  title="{status} - {currentError.title} | NK Technologies"
  description="Error {status} - {currentError.description}"
/>

<div class="min-h-screen bg-[#100A40] text-white flex items-center justify-center px-6">
  <div class="max-w-2xl w-full text-center">
    <!-- Animated Error Code -->
    <div class="mb-8 relative">
      <div class="text-[150px] md:text-[200px] font-bold leading-none">
        <span class="bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent animate-pulse">
          {status}
        </span>
      </div>
      
      <!-- Decorative elements -->
      <div class="absolute inset-0 -z-10">
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-[#ED7D31]/10 rounded-full blur-3xl"></div>
      </div>
    </div>
    
    <!-- Error Title -->
    <h1 class="text-3xl md:text-5xl font-bold mb-4">
      {currentError.title}
    </h1>
    
    <!-- Error Description -->
    <p class="text-xl text-gray-300 mb-3">
      {currentError.description}
    </p>
    
    <p class="text-gray-400 mb-10">
      {currentError.suggestion}
    </p>
    
    <!-- Action Buttons -->
    <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
      <a 
        href="/"
        class="px-8 py-4 bg-gradient-to-r from-[#ED7D31] to-orange-600 text-white font-semibold rounded-lg 
               hover:shadow-lg hover:shadow-[#ED7D31]/50 transition-all transform hover:scale-105
               flex items-center gap-2"
      >
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"/>
        </svg>
        Go to Homepage
      </a>
      
      <button 
        on:click={() => window.history.back()}
        class="px-8 py-4 bg-white/10 backdrop-blur-sm text-white font-semibold rounded-lg border border-white/20 
               hover:bg-white/20 transition-all transform hover:scale-105
               flex items-center gap-2"
      >
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18"/>
        </svg>
        Go Back
      </button>
      
      <a 
        href="/contact"
        class="px-8 py-4 bg-white/10 backdrop-blur-sm text-white font-semibold rounded-lg border border-white/20 
               hover:bg-white/20 transition-all transform hover:scale-105
               flex items-center gap-2"
      >
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
        </svg>
        Contact Us
      </a>
    </div>
    
    <!-- Quick Links -->
    <div class="mt-16 pt-8 border-t border-white/10">
      <p class="text-gray-400 mb-4">You might be looking for:</p>
      <div class="flex flex-wrap justify-center gap-4">
        <a href="/about" class="text-[#ED7D31] hover:text-orange-400 transition-colors">
          About Us
        </a>
        <span class="text-gray-600">•</span>
        <a href="/services" class="text-[#ED7D31] hover:text-orange-400 transition-colors">
          Services
        </a>
        <span class="text-gray-600">•</span>
        <a href="/contact" class="text-[#ED7D31] hover:text-orange-400 transition-colors">
          Contact
        </a>
      </div>
    </div>
  </div>
</div>

<style>
  @keyframes pulse {
    0%, 100% {
      opacity: 1;
    }
    50% {
      opacity: 0.8;
    }
  }
  
  .animate-pulse {
    animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
  }
</style>
