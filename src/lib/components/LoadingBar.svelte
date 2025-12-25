<script>
  import { navigating } from '$app/stores';
  
  $: isNavigating = !!$navigating;
</script>

{#if isNavigating}
  <div class="fixed top-0 left-0 right-0 h-1 bg-transparent z-[100]">
    <div class="h-full bg-gradient-to-r from-[#ED7D31] via-orange-500 to-[#ED7D31] animate-loading-bar"></div>
  </div>
{/if}

<style>
  @keyframes loading-bar {
    0% {
      width: 0%;
      margin-left: 0%;
    }
    50% {
      width: 75%;
      margin-left: 0%;
    }
    100% {
      width: 0%;
      margin-left: 100%;
    }
  }
  
  .animate-loading-bar {
    animation: loading-bar 1.5s ease-in-out infinite;
  }
</style>
