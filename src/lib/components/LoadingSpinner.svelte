<script>
  export let size = 'md'; // 'sm', 'md', 'lg'
  export let color = '#ED7D31';
  
  const sizes = {
    sm: 'w-4 h-4 border-2',
    md: 'w-8 h-8 border-3',
    lg: 'w-12 h-12 border-4'
  };
</script>

<div 
  class="inline-block {sizes[size]} border-t-transparent rounded-full animate-spin"
  style="border-color: {color}; border-top-color: transparent;"
  role="status"
  aria-label="Loading"
>
  <span class="sr-only">Loading...</span>
</div>

<style>
  @keyframes spin {
    to {
      transform: rotate(360deg);
    }
  }
  
  .animate-spin {
    animation: spin 1s linear infinite;
  }
  
  .sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border-width: 0;
  }
</style>
