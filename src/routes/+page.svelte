<svelte:head>
  <title>NK Technologies || Home</title>
</svelte:head>

<script>
  import ModelViewer from '$lib/components/ModelViewer.svelte';
  import SEO from '$lib/components/SEO.svelte';
  import StructuredData from '$lib/components/StructuredData.svelte';
</script>

<SEO 
  title="NK Technologies - Integrated Engineering Solutions | Pune"
  description="Leading Engineering Solutions provider in Pune. Expert services in CAD Design, FEA/CFD Analysis, Advanced Testing, Computer Vision, PLC Automation & Fabrication for Automotive and Defence sectors."
  keywords="engineering solutions pune, CAD design services, FEA analysis, CFD simulation, automotive testing, defence engineering, test fixtures, PLC automation, computer vision, NK Technologies"
  ogImage="/og-home.jpg"
/>

<StructuredData type="Organization" />


<!-- HERO SECTION WITH 3D MODEL -->
<section class="relative min-h-screen bg-nk-bg overflow-hidden">
  <!-- Animated background shapes -->
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <div class="absolute -top-40 -right-40 w-80 h-80 bg-nk-accent/10 rounded-full blur-3xl float" />
    <div class="absolute top-1/3 -left-40 w-80 h-80 bg-cyan-400/5 rounded-full blur-3xl float" style="animation-delay: 2s;" />
    <div class="absolute bottom-0 right-1/4 w-96 h-96 bg-nk-accent/5 rounded-full blur-3xl" style="animation-delay: 4s;" />
  </div>

  <!-- Content -->
  <div class="relative z-10 mx-auto max-w-7xl px-4 sm:px-6 pt-16 pb-12">
    <!-- Hero + 3D Model Grid -->
    <div class="grid gap-8 lg:grid-cols-2 items-start mb-12">
      <!-- Left: Hero Text -->
      <div class="space-y-6 flex flex-col justify-start" style="animation: fadeInUp 0.8s ease-out;">
        <div>
          <span class="inline-block px-3 py-1.5 rounded-full bg-nk-accent/10 text-nk-accent text-xs font-semibold tracking-widest mb-4">
            ✨ DELIVERING INTELLIGENT SOLUTIONS
          </span>
        </div>

        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold leading-tight nk-gradient-text">
          Integrated Technology & Engineering Solutions
        </h1>

        <p class="text-base sm:text-lg text-slate-300 max-w-md leading-relaxed">
          From automotive to defence, we design, simulate, test, and manufacture with precision.
        </p>

        <div class="flex flex-wrap gap-4 pt-2">
          <a
            href="/services"
            class="group inline-flex items-center gap-2 rounded-lg bg-nk-accent px-6 py-2.5 text-sm font-semibold text-slate-950
                   shadow-lg shadow-nk-accent/40 transition transform hover:-translate-y-1 hover:brightness-110 active:scale-95"
          >
            Explore Services
            <svg class="w-4 h-4 group-hover:translate-x-1 transition" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </a>

          <a
            href="/about"
            class="inline-flex items-center gap-2 rounded-lg border border-slate-600 px-6 py-2.5 text-sm font-semibold
                   text-slate-100 transition hover:border-nk-accent hover:text-nk-accent hover:-translate-y-1 active:scale-95"
          >
            Learn More
          </a>
        </div>
      </div>

      <!-- Right: 3D Model -->
      <div class="relative h-80 lg:h-full min-h-80" style="animation: fadeInUp 1s ease-out;">
        <ModelViewer />
      </div>
    </div>
    <!-- Below Hero: Two Column Box Layout -->
    <div class="grid gap-8 lg:grid-cols-2">
      <!-- Left: Engineering Excellence -->
      <div class="relative h-fit" style="animation: fadeInUp 1.1s ease-out;">
        <div class="absolute -inset-0.5 rounded-2xl bg-gradient-to-br from-nk-accent/20 to-cyan-400/20 blur-xl" />
        <div class="relative glass rounded-2xl p-6 md:p-8 space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-3 h-3 rounded-full bg-nk-accent" />
            <h3 class="text-lg font-semibold text-white">Engineering Excellence</h3>
          </div>

          <ul class="space-y-3 text-sm text-slate-300">
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>Design, simulation, testing & manufacturing integrated</span>
            </li>
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>Advanced facilities with real-time monitoring</span>
            </li>
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>Expert engineers with 10+ years experience</span>
            </li>
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>Proven track record in automotive & defence sectors</span>
            </li>
          </ul>
        </div>
      </div>

      <!-- Right: Precision Engineering -->
      <div class="relative h-fit" style="animation: fadeInUp 1.2s ease-out;">
        <div class="absolute -inset-0.5 rounded-2xl bg-gradient-to-br from-nk-accent/20 to-cyan-400/20 blur-xl" />
        <div class="relative glass rounded-2xl p-6 md:p-8 space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-3 h-3 rounded-full bg-nk-accent" />
            <h3 class="text-lg font-semibold text-white">Precision in Action</h3>
          </div>

          <ul class="space-y-3 text-sm text-slate-300">
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>CAD Design & 3D Modelling</span>
            </li>
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>FEA/CFD Analysis & Optimization</span>
            </li>
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>Real-Time Testing & Validation</span>
            </li>
            <li class="flex gap-3">
              <span class="text-nk-accent font-bold">→</span>
              <span>Manufacturing Excellence</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- SERVICES SECTION -->
<section class="relative py-24 md:py-32 bg-gradient-to-b from-nk-bg to-nk-bg/50 gradient-overlay">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <div class="mb-16 space-y-4">
      <span class="inline-block px-3 py-1.5 rounded-full bg-nk-accent/10 text-nk-accent text-xs font-semibold tracking-widest">
        OUR CAPABILITIES
      </span>
      <h2 class="text-4xl md:text-5xl font-bold nk-gradient-text">
        Core Services
      </h2>
      <p class="text-lg text-slate-300 max-w-2xl">
        End-to-end integrated solutions spanning design, simulation, testing, and manufacturing.
      </p>
    </div>

    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      {#each [
        { icon: '🎨', title: 'Design Engineering', desc: '3D CAD, parametric design, optimization' },
        { icon: '⚡', title: 'FEA & CFD Analysis', desc: 'Structural, thermal, aerodynamic' },
        { icon: '🧪', title: 'Advanced Testing', desc: 'Servo, hydraulic, pneumatic systems' },
        { icon: '👁️', title: 'Computer Vision', desc: 'AI-based inspection & quality control' },
        { icon: '⚙️', title: 'PLC Automation', desc: 'HMI, servo drives, VFD control' },
        { icon: '🔧', title: 'Fabrication', desc: 'Welding, machining, assembly' }
      ] as service, index}
        <div
          class="group glass rounded-xl p-6 transition transform hover-lift hover:border-nk-accent/50 fade-in-up"
          style="--index: {index}; animation-delay: calc({index} * 100ms);"
        >
          <div class="mb-4 text-3xl">{service.icon}</div>
          <h3 class="text-lg font-semibold text-white mb-2">{service.title}</h3>
          <p class="text-sm text-slate-400 group-hover:text-slate-300 transition">{service.desc}</p>
          <div class="mt-4 h-1 w-0 bg-gradient-to-r from-nk-accent to-cyan-300 group-hover:w-full transition-all duration-300" />
        </div>
      {/each}
    </div>

    <div class="mt-12 text-center">
      <a href="/services" class="inline-flex items-center gap-2 text-nk-accent hover:text-nk-accent/80 font-semibold transition">
        View all services →
      </a>
    </div>
  </div>
</section>

<!-- WHY CHOOSE US SECTION -->
<section class="relative py-24 md:py-32 bg-nk-bg">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <div class="grid gap-12 lg:grid-cols-2 items-center">
      <div class="space-y-6">
        <span class="inline-block px-3 py-1.5 rounded-full bg-nk-accent/10 text-nk-accent text-xs font-semibold tracking-widest">
          WHY CHOOSE US
        </span>
        <h2 class="text-4xl md:text-5xl font-bold nk-gradient-text">Built for Excellence</h2>
        <p class="text-lg text-slate-300 leading-relaxed">
          With integrated facilities, expert teams, and proven methodologies, we deliver solutions that accelerate development while maintaining the highest standards of quality.
        </p>

        <ul class="space-y-3 text-slate-300">
          {#each ['End-to-end solutions from concept to production', 'Advanced simulation with validated accuracy', 'State-of-the-art facilities with real-time data systems', 'Expert engineers with 10+ years experience', 'Cost-effective solutions with accelerated timelines'] as item}
            <li class="flex gap-3 items-start">
              <svg class="w-5 h-5 text-nk-accent flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
              </svg>
              <span>{item}</span>
            </li>
          {/each}
        </ul>

        <a href="/about" class="inline-flex items-center gap-2 rounded-lg bg-nk-accent px-6 py-3 text-sm font-semibold text-slate-950 shadow-lg shadow-nk-accent/40 transition transform hover:-translate-y-1 hover:brightness-110 active:scale-95">
          Discover Our Story
        </a>
      </div>

      <div class="relative">
        <div class="absolute -inset-4 rounded-2xl bg-gradient-to-br from-nk-accent/15 to-cyan-400/15 blur-2xl" />
        <div class="relative glass rounded-2xl p-8 space-y-6">
          <div class="grid grid-cols-2 gap-4">
            {#each [{ num: '500+', label: 'Dealers & Distributors' }, { num: '16', label: 'Distribution Centers' }, { num: '10+', label: 'Years Expertise' }, { num: '∞', label: 'Possibilities' }] as stat}
              <div class="text-center">
                <div class="text-2xl font-bold text-nk-accent">{stat.num}</div>
                <p class="text-xs text-slate-400 mt-1">{stat.label}</p>
              </div>
            {/each}
          </div>
          <p class="text-sm text-slate-300 border-t border-nk-border pt-6">
            Supporting automotive and defence leaders with robust test fixtures, fire test rigs, durability setups, and special-purpose machines.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA SECTION -->
<section class="relative py-20 md:py-28 bg-gradient-to-b from-nk-bg via-nk-bg to-nk-bg/80">
  <div class="mx-auto max-w-4xl px-4 sm:px-6 text-center space-y-6">
    <h2 class="text-3xl md:text-5xl font-bold nk-gradient-text">
      Ready to Transform Your Project?
    </h2>
    <p class="text-lg text-slate-300 max-w-2xl mx-auto">
      Connect with our team to discuss how NK Technologies can bring your vision to life with integrated engineering solutions.
    </p>

    <div class="flex flex-wrap gap-4 justify-center pt-4">
      <a
        href="/contact"
        class="inline-flex items-center gap-2 rounded-lg bg-nk-accent px-8 py-3 text-sm font-semibold text-slate-950
               shadow-lg shadow-nk-accent/40 transition transform hover:-translate-y-1 hover:brightness-110 active:scale-95"
      >
        Start a Conversation
      </a>

      <a
        href="tel:+919730553516"
        class="inline-flex items-center gap-2 rounded-lg border border-slate-600 px-8 py-3 text-sm font-semibold
               text-slate-100 transition hover:border-nk-accent hover:text-nk-accent hover:-translate-y-1 active:scale-95"
      >
        <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
          <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773c.26.559.738 1.3 1.948 2.51 1.21 1.21 1.951 1.688 2.51 1.948l.773-1.548a1 1 0 011.06-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 4 14.18 4 9.5S7.82 2 12.5 2h2a1 1 0 011 1z" />
        </svg>
        Call +91-97305 53516
      </a>
    </div>
  </div>
</section>
