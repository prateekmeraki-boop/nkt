<script>
  export let type = 'Organization';
  export let data = {};
  
  const organizationData = {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "NK Technologies",
    "url": "https://nk-technologies.com",
    "logo": "https://nk-technologies.com/logo.svg",
    "description": "Integrated Technology & Engineering Solutions company for Automotive and Defence sectors",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "Near Katraj-Dehu Rd Bypass, C'Lai World, opp. Podar International School, Ambegaon Budruk",
      "addressLocality": "Pune",
      "addressRegion": "Maharashtra",
      "postalCode": "411046",
      "addressCountry": "IN"
    },
    "contactPoint": {
      "@type": "ContactPoint",
      "telephone": "+91-97305-53516",
      "contactType": "Customer Service",
      "email": "karan@nk-technologies.com",
      "availableLanguage": ["English", "Hindi"]
    },
    "sameAs": [
      "https://linkedin.com/company/nk-technologies"
    ],
    "founder": [
      {
        "@type": "Person",
        "name": "Mr. Nikhil Mate"
      },
      {
        "@type": "Person",
        "name": "Mr. Karan Kamble"
      }
    ]
  };
  
  $: structuredData = type === 'Organization' ? organizationData : data;
</script>

<svelte:head>
  {@html `<script type="application/ld+json">${JSON.stringify(structuredData)}</script>`}
</svelte:head>
