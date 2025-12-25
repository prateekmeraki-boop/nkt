<script>
  export let title = 'NK Technologies - Engineering Solutions';
  export let description = 'Integrated Technology & Engineering Solutions for Automotive and Defence sectors. Expert CAD, FEA, CFD, Testing, and Automation services.';
  export let keywords = 'engineering solutions, CAD design, FEA analysis, CFD, automotive testing, defence engineering, PLC automation, computer vision, Pune';
  export let ogImage = '/og-image.jpg';
  export let ogType = 'website';
  export let canonicalUrl = '';
  
  // Get current URL for canonical
  import { page } from '$app/stores';
  $: currentUrl = canonicalUrl || `https://nk-technologies.com${$page.url.pathname}`;
</script>

<svelte:head>
  <!-- Primary Meta Tags -->
  <title>{title}</title>
  <meta name="title" content={title} />
  <meta name="description" content={description} />
  <meta name="keywords" content={keywords} />
  <meta name="author" content="NK Technologies" />
  <meta name="robots" content="index, follow" />
  <link rel="canonical" href={currentUrl} />
  
  <!-- Open Graph / Facebook -->
  <meta property="og:type" content={ogType} />
  <meta property="og:url" content={currentUrl} />
  <meta property="og:title" content={title} />
  <meta property="og:description" content={description} />
  <meta property="og:image" content={ogImage} />
  <meta property="og:site_name" content="NK Technologies" />
  
  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content={currentUrl} />
  <meta property="twitter:title" content={title} />
  <meta property="twitter:description" content={description} />
  <meta property="twitter:image" content={ogImage} />
  
  <!-- Additional Meta Tags -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="theme-color" content="#100A40" />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
  
  <!-- Language -->
  <meta http-equiv="content-language" content="en" />
  <html lang="en" />
</svelte:head>
