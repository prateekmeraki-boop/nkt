<script lang="ts">
  export let label: string;
</script>

<!-- Just wraps the icon for consistent sizing & tooltip -->
<div class="group relative flex h-10 w-10 items-center justify-center rounded-full bg-nk-surface border border-nk-border
            shadow-md hover:-translate-y-0.5 hover:bg-nk-accent transition transform active:scale-95">
  <slot />

  <!-- Tooltip -->
  <span
    class="pointer-events-none absolute left-12 top-1/2 -translate-y-1/2 rounded-md bg-black/80 px-2 py-1
           text-[10px] font-medium text-white opacity-0 group-hover:opacity-100 transition-opacity"
  >
    {label}
  </span>
</div>
