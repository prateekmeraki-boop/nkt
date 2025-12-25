<script>
  import SEO from '$lib/components/SEO.svelte';
  // ... rest of your imports
</script>

<SEO 
  title="About NK Technologies - Engineering Excellence Since 2015"
  description="Learn about NK Technologies, founded by Mr. Nikhil Mate and Mr. Karan Kamble. We deliver integrated engineering solutions to automotive and defence leaders with 10+ years of expertise."
  keywords="about NK Technologies, engineering company pune, Nikhil Mate, Karan Kamble, automotive engineering, defence solutions"
  ogImage="/og-about.jpg"
/>


<svelte:head>
  <title>NK Technologies || About</title>
</svelte:head>

<!-- HERO SECTION WITH REAL IMAGE -->
<section class="relative min-h-fit bg-nk-bg overflow-hidden pt-20 pb-16">
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <div class="absolute -top-40 -right-40 w-80 h-80 bg-nk-accent/10 rounded-full blur-3xl float" />
    <div class="absolute top-1/3 -left-40 w-80 h-80 bg-cyan-400/5 rounded-full blur-3xl float" style="animation-delay: 2s;" />
  </div>

  <div class="relative z-10 mx-auto max-w-7xl px-4 sm:px-6">
    <div class="grid gap-12 lg:grid-cols-2 items-center">
      <div class="space-y-6">
        <span class="inline-block px-3 py-1.5 rounded-full bg-nk-accent/10 text-nk-accent text-xs font-semibold tracking-widest">
          OUR STORY
        </span>
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold leading-tight nk-gradient-text">
          About NK Technologies
        </h1>
        <p class="text-lg text-slate-300 max-w-2xl leading-relaxed">
          A service-based Technology & Engineering Solutions company committed to delivering speedy and cost-effective
          services and products without compromising on quality.
        </p>
      </div>

      <!-- Hero Image -->
      <div class="relative h-80 rounded-2xl overflow-hidden">
        <img 
          src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=600&h=400&fit=crop" 
          alt="Modern Manufacturing Facility" 
          class="w-full h-full object-cover"
        />
        <div class="absolute inset-0 bg-gradient-to-t from-nk-bg/60 to-transparent" />
      </div>
    </div>
  </div>
</section>

<!-- COMPANY OVERVIEW WITH IMAGE -->
<section class="relative py-24 md:py-32 bg-nk-bg">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <div class="grid gap-12 lg:grid-cols-2 items-center mb-16">
      <div class="space-y-6">
        <h2 class="text-3xl md:text-4xl font-bold nk-gradient-text">Who We Are</h2>
        <div class="space-y-4 text-slate-300">
          <p class="text-base leading-relaxed">
            NK Technologies is the brainchild of <span class="font-semibold">Mr. Nikhil Mate</span> and
            <span class="font-semibold">Mr. Karan Kamble</span>, both engineers and entrepreneurs with a shared vision to
            revolutionize the manufacturing and engineering solutions landscape in India.
          </p>
          <p class="text-base leading-relaxed">
            We are an integrated engineering solutions provider for the <span class="font-semibold">automotive and defence</span> sectors,
            bringing expertise spanning design, simulation, testing, and manufacturing under one roof.
          </p>
          <p class="text-base leading-relaxed">
            Our journey is built on the belief that innovation thrives when brilliant minds have access to world-class
            facilities, proven methodologies, and a culture of continuous improvement.
          </p>
        </div>
      </div>

      <div class="relative">
        <div class="absolute -inset-4 rounded-2xl bg-gradient-to-br from-nk-accent/15 to-cyan-400/15 blur-2xl" />
        <div class="relative glass rounded-2xl p-8 space-y-6">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-nk-accent to-cyan-300 flex items-center justify-center">
              <span class="text-xl">📍</span>
            </div>
            <h3 class="text-xl font-bold text-white">Quick Facts</h3>
          </div>
          <div class="space-y-4">
            <div class="border-b border-nk-border pb-4">
              <p class="text-sm text-slate-400 mb-1">Headquarters</p>
              <p class="text-white font-semibold">Pune, Maharashtra, India</p>
            </div>
            <div class="border-b border-nk-border pb-4">
              <p class="text-sm text-slate-400 mb-1">Industry Focus</p>
              <p class="text-white font-semibold">Automotive & Defence</p>
            </div>
            <div class="border-b border-nk-border pb-4">
              <p class="text-sm text-slate-400 mb-1">Core Strength</p>
              <p class="text-white font-semibold">Integrated Engineering Solutions</p>
            </div>
            <div>
              <p class="text-sm text-slate-400 mb-1">Distribution Network</p>
              <p class="text-white font-semibold">500+ Dealers & 16 Distributors</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- MISSION & VISION WITH IMAGES - BALANCED -->
<section class="relative py-24 md:py-32 bg-gradient-to-b from-nk-bg to-nk-bg/50">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-3xl md:text-4xl font-bold nk-gradient-text mb-16 text-center">Mission & Vision</h2>

    <div class="grid gap-8 md:grid-cols-2 mb-16">
      <!-- Mission -->
      <div class="relative group">
        <div class="absolute -inset-0.5 rounded-2xl bg-gradient-to-br from-nk-accent/20 to-cyan-400/20 blur-xl opacity-0 group-hover:opacity-100 transition" />
        <div class="relative glass rounded-2xl overflow-hidden h-full flex flex-col">
          <img 
            src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=350&fit=crop" 
            alt="Team Working Together" 
            class="w-full h-48 object-cover group-hover:scale-105 transition duration-300"
          />
          <div class="p-8 space-y-4 flex-grow">
            <h3 class="text-2xl font-bold text-nk-accent">Our Mission</h3>
            <div class="space-y-3 text-slate-300">
              <p class="text-sm leading-relaxed">
                To ensure the highest standards of social responsibility while delivering innovative engineering solutions that create tangible impact.
              </p>
              <ul class="space-y-2 text-sm">
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">✓</span>
                  <span>Exceed customer business requirements and challenges</span>
                </li>
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">✓</span>
                  <span>Deliver highest quality service with speed and efficiency</span>
                </li>
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">✓</span>
                  <span>Create an environment for collective growth and innovation</span>
                </li>
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">✓</span>
                  <span>Foster ethical practices in all business dealings</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Vision -->
      <div class="relative group">
        <div class="absolute -inset-0.5 rounded-2xl bg-gradient-to-br from-nk-accent/20 to-cyan-400/20 blur-xl opacity-0 group-hover:opacity-100 transition" />
        <div class="relative glass rounded-2xl overflow-hidden h-full flex flex-col">
          <img 
            src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?w=600&h=350&fit=crop" 
            alt="Future Innovation Technology" 
            class="w-full h-48 object-cover group-hover:scale-105 transition duration-300"
          />
          <div class="p-8 space-y-4 flex-grow">
            <h3 class="text-2xl font-bold text-nk-accent">Our Vision</h3>
            <div class="space-y-3 text-slate-300">
              <p class="text-sm leading-relaxed">
                To bridge the gap in the manufacturing sector and empower innovators to transform brilliant ideas into market-leading products.
              </p>
              <ul class="space-y-2 text-sm">
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">→</span>
                  <span>Enable engineers and entrepreneurs with integrated end-to-end solutions</span>
                </li>
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">→</span>
                  <span>Provide world-class facilities meeting international standards</span>
                </li>
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">→</span>
                  <span>Accelerate product development from concept to commercialization</span>
                </li>
                <li class="flex gap-3">
                  <span class="text-nk-accent font-bold">→</span>
                  <span>Transform innovative ideas into best-selling products</span>
                </li>
              </ul>
              <p class="text-sm font-semibold text-nk-accent pt-2">
                Goal: Be the trusted partner turning concepts into market success.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- CORE COMPETENCIES WITH IMAGES -->
<section class="relative py-24 md:py-32 bg-nk-bg">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-3xl md:text-4xl font-bold nk-gradient-text mb-16">Core Competencies</h2>

    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      {#each [
        {
          title: 'Design Engineering',
          image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=300&fit=crop',
          items: ['3D CAD modeling', 'Parametric design', 'Light-weighting', 'Material selection']
        },
        {
          title: 'FEA & CFD Analysis',
          image: 'https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=400&h=300&fit=crop',
          items: ['Structural analysis', 'Thermal simulation', 'Aerodynamic optimization', 'Fatigue analysis']
        },
        {
          title: 'Advanced Testing',
          image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=300&fit=crop',
          items: ['Servo-electric systems', 'Hydraulic testing', 'Pneumatic cycling', 'Data acquisition']
        },
        {
          title: 'Computer Vision & AI',
          image: 'https://images.unsplash.com/photo-1535820727271-a6e6904d0ff2?w=400&h=300&fit=crop',
          items: ['Defect detection', 'Real-time inspection', 'ML classification', 'Video analytics']
        },
        {
          title: 'PLC & Automation',
          image: 'https://images.unsplash.com/photo-1504384308090-c894fdcc538d?w=400&h=300&fit=crop',
          items: ['PLC programming', 'HMI development', 'Servo control', 'Multi-axis sync']
        },
        {
          title: 'Fabrication & Machining',
          image: 'https://images.unsplash.com/photo-1621905251918-48416bd8575a?w=400&h=300&fit=crop',
          items: ['Arc welding', 'Precision assembly', 'Surface treatment', 'Final testing']
        }
      ] as comp}
        <div class="group glass rounded-xl overflow-hidden transition transform hover-lift hover:border-nk-accent/50">
          <img 
            src={comp.image} 
            alt={comp.title} 
            class="w-full h-40 object-cover group-hover:scale-105 transition duration-300"
          />
          <div class="p-6 space-y-3">
            <h3 class="text-lg font-semibold text-white">{comp.title}</h3>
            <ul class="space-y-1">
              {#each comp.items as item}
                <li class="flex gap-2 text-sm text-slate-300">
                  <span class="text-nk-accent">•</span>
                  <span>{item}</span>
                </li>
              {/each}
            </ul>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- PORTFOLIO WITH IMAGES -->
<section class="relative py-24 md:py-32 bg-gradient-to-b from-nk-bg to-nk-bg/50">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-3xl md:text-4xl font-bold nk-gradient-text mb-16">Portfolio & Achievements</h2>

    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      {#each [
        { title: 'Vibration & Shock Testing', image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=300&fit=crop', desc: 'Battery packs, motors, automotive components' },
        { title: 'Durability Test Setups', image: 'https://images.unsplash.com/photo-1504384308090-c894fdcc538d?w=400&h=300&fit=crop', desc: 'Hand brakes, springs, mechanical assemblies' },
        { title: 'Fire Test Rigs', image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=300&fit=crop', desc: 'AIS standards compliance testing' },
        { title: 'Quality Fixtures', image: 'https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=400&h=300&fit=crop', desc: 'Precision verification & assurance' },
        { title: 'Environmental Testing', image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=300&fit=crop', desc: 'Temperature & humidity chambers' },
        { title: 'Custom Fabrication', image: 'https://images.unsplash.com/photo-1621905251918-48416bd8575a?w=400&h=300&fit=crop', desc: 'Large-scale test fixtures & assemblies' }
      ] as item}
        <div class="relative group">
          <div class="absolute -inset-0.5 rounded-2xl bg-gradient-to-br from-nk-accent/10 to-cyan-400/10 blur-lg opacity-0 group-hover:opacity-100 transition" />
          <div class="relative glass rounded-2xl overflow-hidden h-full flex flex-col">
            <img 
              src={item.image} 
              alt={item.title} 
              class="w-full h-40 object-cover group-hover:scale-105 transition duration-300"
            />
            <div class="p-6 space-y-3 flex-grow flex flex-col justify-between">
              <div>
                <h4 class="text-lg font-semibold text-nk-accent mb-2">{item.title}</h4>
                <p class="text-sm text-slate-300">{item.desc}</p>
              </div>
            </div>
          </div>
        </div>
      {/each}
    </div>


      <!-- Clients Section with Real Logos -->
    <div class="space-y-8 mt-16">
      <h3 class="text-2xl font-bold text-white">Esteemed Clients</h3>
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        {#each [
          { name: 'Mahindra Electric', file: 'mahindra-electric.svg' },
          { name: 'Morris Garages', file: 'mg-motor.svg' },
          { name: 'Spark Minda', file: 'spark-minda.svg' },
          { name: 'Tata Motors', file: 'tata-motors.svg' },
          { name: 'Tata Autocomp', file: 'tata-autocomp.png' },
          { name: 'Euler Motors', file: 'euler-motors.svg' },
          { name: 'Sun Mobility', file: 'sun-mobility.png' },
          { name: 'Wittur', file: 'wittur.svg' }
        ] as client}
          <div class="glass rounded-lg p-6 flex items-center justify-center hover:border-nk-accent/50 hover:-translate-y-1 transition transform min-h-32">
            <img 
              src="/logos/{client.file}" 
              alt={client.name}
              class="h-16 w-auto max-w-full object-contain filter brightness-0 invert hover:scale-110 transition"
            />
          </div>
        {/each}
      </div>
    </div>


  </div>
</section>

<!-- WHY CHOOSE US WITH IMAGES -->
<section class="relative py-24 md:py-32 bg-nk-bg">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-3xl md:text-4xl font-bold nk-gradient-text mb-16 text-center">Why Choose NK Technologies</h2>

    <div class="grid gap-8 md:grid-cols-2">
      {#each [
        { icon: '🏭', title: 'Integrated Facilities', desc: 'Design, simulation, testing, and manufacturing all under one roof for seamless execution', image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=600&h=400&fit=crop' },
        { icon: '⚡', title: 'Advanced Technology', desc: 'State-of-the-art equipment with real-time monitoring and data acquisition systems', image: 'https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=600&h=400&fit=crop' },
        { icon: '👨‍💼', title: 'Expert Team', desc: 'Engineers with 10+ years of industry experience in automotive and defence sectors', image: 'https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=400&fit=crop' },
        { icon: '⚙️', title: 'Quality Assurance', desc: 'Rigorous testing protocols and compliance with international standards and codes', image: 'https://images.unsplash.com/photo-1504384308090-c894fdcc538d?w=600&h=400&fit=crop' },
        { icon: '🚀', title: 'Rapid Turnaround', desc: 'Cost-effective solutions with accelerated timelines without compromising quality', image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=600&h=400&fit=crop' },
        { icon: '🤝', title: 'Customer Focus', desc: 'Collaborative approach to understand and exceed customer business requirements', image: 'https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=400&fit=crop' }
      ] as item}
        <div class="relative group">
          <div class="absolute -inset-0.5 rounded-2xl bg-gradient-to-br from-nk-accent/15 to-cyan-400/10 blur-lg opacity-0 group-hover:opacity-100 transition" />
          <div class="relative glass rounded-2xl overflow-hidden h-full flex flex-col">
            <img 
              src={item.image} 
              alt={item.title} 
              class="w-full h-48 object-cover group-hover:scale-110 transition duration-300"
            />
            <div class="p-8 space-y-3 flex-grow">
              <div class="flex items-center gap-3">
                <div class="text-4xl">{item.icon}</div>
                <h4 class="text-lg font-bold text-white">{item.title}</h4>
              </div>
              <p class="text-sm text-slate-300">{item.desc}</p>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- STATS SECTION WITH VISUAL DESIGN -->
<section class="relative py-24 md:py-32 bg-gradient-to-b from-nk-bg to-nk-bg/50">
  <div class="mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-3xl md:text-4xl font-bold nk-gradient-text mb-16 text-center">Our Impact</h2>
    <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
      {#each [
        { icon: '📊', num: '500+', label: 'Dealers & Distributors' },
        { icon: '🌍', num: '16', label: 'Distribution Centers' },
        { icon: '⭐', num: '10+', label: 'Years Expertise' },
        { icon: '✅', num: '50+', label: 'Projects Delivered' }
      ] as stat}
        <div class="glass rounded-xl p-8 text-center space-y-3 hover:border-nk-accent/50 transition transform hover:-translate-y-1">
          <div class="text-4xl text-center">{stat.icon}</div>
          <div class="text-4xl md:text-5xl font-bold text-nk-accent">{stat.num}</div>
          <p class="text-sm text-slate-300">{stat.label}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- CTA SECTION -->
<section class="relative py-20 md:py-28 bg-gradient-to-b from-nk-bg via-nk-bg to-nk-bg/80">
  <div class="mx-auto max-w-4xl px-4 sm:px-6 text-center space-y-6">
    <h2 class="text-3xl md:text-5xl font-bold nk-gradient-text">
      Ready to Partner With Us?
    </h2>
    <p class="text-lg text-slate-300 max-w-2xl mx-auto">
      Discover how NK Technologies can be your trusted partner in transforming engineering challenges into competitive advantages.
    </p>

    <div class="flex flex-wrap gap-4 justify-center pt-4">
      <a
        href="/contact"
        class="inline-flex items-center gap-2 rounded-lg bg-nk-accent px-8 py-3 text-sm font-semibold text-slate-950
               shadow-lg shadow-nk-accent/40 transition transform hover:-translate-y-1 hover:brightness-110 active:scale-95"
      >
        Get in Touch
      </a>

      <a
        href="/services"
        class="inline-flex items-center gap-2 rounded-lg border border-slate-600 px-8 py-3 text-sm font-semibold
               text-slate-100 transition hover:border-nk-accent hover:text-nk-accent hover:-translate-y-1 active:scale-95"
      >
        Explore Services
      </a>
    </div>
  </div>
</section>
