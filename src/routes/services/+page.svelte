<script>
  import { onMount } from 'svelte';
  import SEO from '$lib/components/SEO.svelte';
  
  let mounted = false;
  
  onMount(() => {
    mounted = true;
  });
</script>

<SEO 
  title="Engineering Services - Design, Testing, Automation | NK Technologies"
  description="Comprehensive engineering services: Design Engineering, FEA & CFD Analysis, Advanced Testing Systems, Computer Vision, PLC Automation, and Fabrication. Serving automotive and defence industries."
  keywords="design engineering, FEA services, CFD analysis, advanced testing, computer vision AI, PLC automation services, fabrication machining, engineering services pune"
  ogImage="/og-services.jpg"
/>

<svelte:head>
  <title>NK Technologies || Services</title>
</svelte:head>

<div class="min-h-screen bg-[#100A40] text-white">
  <!-- Hero Section -->
  <section class="relative overflow-hidden pt-24 pb-20">
    <div class="absolute inset-0 opacity-10">
      <div class="absolute inset-0 bg-gradient-to-br from-[#ED7D31] via-transparent to-transparent"></div>
    </div>
    
    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center max-w-4xl mx-auto">
        <p class="text-[#ED7D31] text-sm font-semibold tracking-wider mb-4">OUR EXPERTISE</p>
        <h1 class="text-5xl md:text-6xl font-bold mb-6 bg-gradient-to-r from-white via-gray-200 to-gray-400 bg-clip-text text-transparent">
          Services Offered
        </h1>
        <p class="text-lg text-gray-300 mb-8">
          NK Technologies delivers integrated services across design engineering, FEA & CFD analysis, 
          advanced test systems, computer vision, automation, and fabrication to support complex engineering challenges.
        </p>
      </div>
    </div>
  </section>

  <!-- Design Engineering Section -->
  <section class="py-16 relative">
    <div class="container mx-auto px-6">
      <div class="grid md:grid-cols-2 gap-12 items-center mb-16">
        <div class="order-2 md:order-1" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out;">
          <img 
            src="https://images.unsplash.com/photo-1581094794329-c8112a89af12?w=800&q=80" 
            alt="CAD Design" 
            class="rounded-xl shadow-2xl w-full"
          />
        </div>
        
        <div class="order-1 md:order-2" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.2s;">
          <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
            Design Engineering & 3D Modelling
          </h2>
          
          <p class="text-gray-300 mb-6">
            Transform your concepts into reality with our comprehensive design engineering services. 
            We leverage cutting-edge CAD tools and parametric design techniques to deliver optimized solutions.
          </p>
          
          <div class="space-y-4">
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Concept Design & Feasibility Studies</h4>
                <p class="text-sm text-gray-400">Validate your ideas with comprehensive feasibility analysis</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">3D CAD Modelling & Parametric Design</h4>
                <p class="text-sm text-gray-400">Precision modeling with full parametric control</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Detailed Engineering Drawings</h4>
                <p class="text-sm text-gray-400">Manufacturing-ready technical documentation</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Design Optimization & Light-weighting</h4>
                <p class="text-sm text-gray-400">Maximize performance while minimizing weight and cost</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Material Selection & Analysis</h4>
                <p class="text-sm text-gray-400">Expert guidance on optimal material choices</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Decorative Divider -->
  <div class="container mx-auto px-6">
    <div class="h-px bg-gradient-to-r from-transparent via-[#ED7D31] to-transparent"></div>
  </div>
  <!-- FEA & CFD Analysis Section -->
  <section class="py-16 relative">
    <div class="container mx-auto px-6">
      <div class="grid md:grid-cols-2 gap-12 items-center mb-16">
        <div class="order-1" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.4s;">
          <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
            FEA & CFD Analysis
          </h2>
          
          <p class="text-gray-300 mb-6">
            Predict performance, validate designs, and optimize products before physical prototyping. 
            Our advanced simulation capabilities cover structural, thermal, and fluid dynamics analysis.
          </p>
          
          <div class="grid grid-cols-1 gap-4">
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Structural Analysis</h4>
              <p class="text-sm text-gray-400">Static and dynamic analysis, non-linear and contact simulations</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Vibration & Noise Analysis</h4>
              <p class="text-sm text-gray-400">Harmonic, shock, and vibration analysis for NVH optimization</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Fatigue & Durability</h4>
              <p class="text-sm text-gray-400">Life prediction and durability assessment</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Thermal Management</h4>
              <p class="text-sm text-gray-400">Heat transfer analysis and thermal optimization</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Aerodynamics & Fluid Flow</h4>
              <p class="text-sm text-gray-400">CFD analysis, drag optimization, HVAC simulations</p>
            </div>
          </div>
        </div>
        
        <div class="order-2" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.6s;">
          <img 
            src="https://images.unsplash.com/photo-1635070041078-e363dbe005cb?w=800&q=80" 
            alt="FEA Analysis" 
            class="rounded-xl shadow-2xl w-full"
          />
        </div>
      </div>
    </div>
  </section>

  <!-- Decorative Divider -->
  <div class="container mx-auto px-6">
    <div class="h-px bg-gradient-to-r from-transparent via-[#ED7D31] to-transparent"></div>
  </div>
  <!-- Advanced Testing Systems Section -->
  <section class="py-16 relative">
    <div class="container mx-auto px-6">
      <div class="text-center mb-12">
        <h2 class="text-4xl font-bold mb-4 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
          Advanced Test Systems
        </h2>
        <p class="text-gray-300 max-w-3xl mx-auto">
          State-of-the-art testing infrastructure with precision control systems and real-time data acquisition
        </p>
      </div>
      
      <div class="grid md:grid-cols-3 gap-8 mb-12">
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:border-[#ED7D31]/50 transition-all group">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">⚡</span>
          </div>
          <h3 class="text-xl font-bold mb-3">Servo-Electric Systems</h3>
          <p class="text-gray-400 text-sm">
            Precision control systems for high-accuracy testing with multi-axis coordination
          </p>
        </div>
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:border-[#ED7D31]/50 transition-all group">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">💪</span>
          </div>
          <h3 class="text-xl font-bold mb-3">Hydraulic Testing</h3>
          <p class="text-gray-400 text-sm">
            Heavy-load testing capabilities with hydraulic frames and actuators
          </p>
        </div>
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:border-[#ED7D31]/50 transition-all group">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">🔄</span>
          </div>
          <h3 class="text-xl font-bold mb-3">Pneumatic Cycling</h3>
          <p class="text-gray-400 text-sm">
            Rapid cycling actuators for durability and endurance testing
          </p>
        </div>
      </div>
      
      <div class="bg-gradient-to-br from-white/5 to-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/10">
        <div class="grid md:grid-cols-2 gap-8 items-center">
          <div>
            <h3 class="text-2xl font-bold mb-4">Real-Time Data Acquisition</h3>
            <p class="text-gray-300 mb-4">
              Advanced DAQ systems for comprehensive monitoring and analysis during testing
            </p>
            <ul class="space-y-2">
              <li class="flex items-center gap-2">
                <span class="text-[#ED7D31]">✓</span>
                <span class="text-sm text-gray-300">Multi-channel data logging</span>
              </li>
              <li class="flex items-center gap-2">
                <span class="text-[#ED7D31]">✓</span>
                <span class="text-sm text-gray-300">Real-time visualization</span>
              </li>
              <li class="flex items-center gap-2">
                <span class="text-[#ED7D31]">✓</span>
                <span class="text-sm text-gray-300">Automated reporting</span>
              </li>
            </ul>
          </div>
          <div>
            <img 
              src="https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=600&q=80" 
              alt="Testing Equipment" 
              class="rounded-lg shadow-xl"
            />
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Decorative Divider -->
  <div class="container mx-auto px-6">
    <div class="h-px bg-gradient-to-r from-transparent via-[#ED7D31] to-transparent"></div>
  </div>

  <!-- Computer Vision & AI Section -->
  <section class="py-16 relative">
    <div class="container mx-auto px-6">
      <div class="grid md:grid-cols-2 gap-12 items-center mb-16">
        <div class="order-2 md:order-1" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out;">
          <img 
            src="https://images.unsplash.com/photo-1677442136019-21780ecad995?w=800&q=80" 
            alt="AI Vision" 
            class="rounded-xl shadow-2xl w-full"
          />
        </div>
        
        <div class="order-1 md:order-2" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.2s;">
          <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
            Computer Vision & Image Processing
          </h2>
          
          <p class="text-gray-300 mb-6">
            Computer vision-based products using AI support industrial automation, inspection, and 
            decision-making with reduced human intervention.
          </p>
          
          <div class="space-y-4">
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Real-time Inspection & Defect Detection</h4>
                <p class="text-sm text-gray-400">Automated quality control with ML-based classification</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">High-speed Deformation Tracking</h4>
                <p class="text-sm text-gray-400">Precision measurement during dynamic tests</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Video Analytics & Data Logging</h4>
                <p class="text-sm text-gray-400">Comprehensive analysis and documentation</p>
              </div>
            </div>
            
            <div class="flex items-start gap-3 group">
              <div class="w-2 h-2 bg-[#ED7D31] rounded-full mt-2 group-hover:scale-150 transition-transform"></div>
              <div>
                <h4 class="font-semibold text-white">Industry Applications</h4>
                <p class="text-sm text-gray-400">Agriculture, healthcare, automotive, banking, retail, OCR, and more</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Decorative Divider -->
  <div class="container mx-auto px-6">
    <div class="h-px bg-gradient-to-r from-transparent via-[#ED7D31] to-transparent"></div>
  </div>
  <!-- PLC & Automation Section -->
  <section class="py-16 relative">
    <div class="container mx-auto px-6">
      <div class="grid md:grid-cols-2 gap-12 items-center mb-16">
        <div class="order-1" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.4s;">
          <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
            PLC, HMI & Servo Drive Automation
          </h2>
          
          <p class="text-gray-300 mb-6">
            NK Technologies provides smart automation solutions across PLC, HMI, servo, and VFD platforms 
            for modern industrial systems.
          </p>
          
          <div class="grid grid-cols-1 gap-4">
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">PLC Programming & Commissioning</h4>
              <p class="text-sm text-gray-400">Complete ladder logic development and system integration</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">HMI Development & Integration</h4>
              <p class="text-sm text-gray-400">Intuitive operator interfaces for control systems</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Servo Drives & VFD Control</h4>
              <p class="text-sm text-gray-400">Position, speed, and multi-axis synchronization</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Machine & Process Automation</h4>
              <p class="text-sm text-gray-400">End-to-end automation solutions</p>
            </div>
            
            <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10 hover:border-[#ED7D31]/50 transition-all">
              <h4 class="font-semibold text-white mb-2">Interfacing & Communications</h4>
              <p class="text-sm text-gray-400">Sensors, encoders, Serial, Modbus, CC-Link, SSCNET protocols</p>
            </div>
          </div>
        </div>
        
        <div class="order-2" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.6s;">
          <img 
            src="https://images.unsplash.com/photo-1586864387634-80fea04fca77?w=800&q=80" 
            alt="Industrial Automation" 
            class="rounded-xl shadow-2xl w-full"
          />
        </div>
      </div>
    </div>
  </section>

  <!-- Decorative Divider -->
  <div class="container mx-auto px-6">
    <div class="h-px bg-gradient-to-r from-transparent via-[#ED7D31] to-transparent"></div>
  </div>
  <!-- Fabrication Section -->
  <section class="py-16 relative">
    <div class="container mx-auto px-6">
      <div class="text-center mb-12">
        <h2 class="text-4xl font-bold mb-4 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
          Fabrication & Machining
        </h2>
        <p class="text-gray-300 max-w-3xl mx-auto">
          Complete fabrication services from welding to final assembly with precision quality control
        </p>
      </div>
      
      <div class="grid md:grid-cols-3 gap-8 mb-12">
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:border-[#ED7D31]/50 transition-all group">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">🔥</span>
          </div>
          <h3 class="text-xl font-bold mb-3">Gas & Arc Welding</h3>
          <p class="text-gray-400 text-sm">
            Expert welding services for various materials and applications
          </p>
        </div>
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:border-[#ED7D31]/50 transition-all group">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">⚙️</span>
          </div>
          <h3 class="text-xl font-bold mb-3">Precision Assembly</h3>
          <p class="text-gray-400 text-sm">
            Sub-assembly and test fixture fabrication with tight tolerances
          </p>
        </div>
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:border-[#ED7D31]/50 transition-all group">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">✨</span>
          </div>
          <h3 class="text-xl font-bold mb-3">Surface Treatment</h3>
          <p class="text-gray-400 text-sm">
            Coating, finishing, and final testing services
          </p>
        </div>
      </div>
      
      <div class="grid md:grid-cols-2 gap-8">
        <img 
          src="https://images.unsplash.com/photo-1565193566173-7a0ee3dbe261?w=600&q=80" 
          alt="Welding" 
          class="rounded-lg shadow-xl w-full h-64 object-cover"
        />
        <img 
          src="https://images.unsplash.com/photo-1581092795360-fd1ca04f0952?w=600&q=80" 
          alt="Manufacturing" 
          class="rounded-lg shadow-xl w-full h-64 object-cover"
        />
      </div>
    </div>
  </section>

  <!-- Standards Section -->
  <section class="py-16 bg-gradient-to-br from-white/5 to-transparent">
    <div class="container mx-auto px-6">
      <div class="max-w-4xl mx-auto text-center">
        <div class="inline-block p-3 bg-[#ED7D31]/10 rounded-full mb-6">
          <span class="text-4xl">📋</span>
        </div>
        
        <h2 class="text-3xl font-bold mb-4 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
          Exposure to Design Codes
        </h2>
        
        <p class="text-gray-300 mb-8">
          Our team has extensive experience with international design codes and standards, ensuring 
          compliance and quality in every project.
        </p>
        
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
          <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10">
            <p class="font-semibold text-[#ED7D31]">AIS 038</p>
            <p class="text-xs text-gray-400 mt-1">Automotive Standards</p>
          </div>
          <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10">
            <p class="font-semibold text-[#ED7D31]">AIS 156</p>
            <p class="text-xs text-gray-400 mt-1">Battery Safety</p>
          </div>
          <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10">
            <p class="font-semibold text-[#ED7D31]">UN 38.3</p>
            <p class="text-xs text-gray-400 mt-1">Transport Testing</p>
          </div>
          <div class="bg-white/5 backdrop-blur-sm p-4 rounded-lg border border-white/10">
            <p class="font-semibold text-[#ED7D31]">ASME</p>
            <p class="text-xs text-gray-400 mt-1">Engineering Codes</p>
          </div>
        </div>
      </div>
    </div>
  </section>

    <!-- Call to Action Section -->
  <section class="py-20 relative overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-br from-[#ED7D31]/10 to-transparent"></div>
    
    <div class="container mx-auto px-6 relative z-10">
      <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
          Ready to Elevate Your Project?
        </h2>
        
        <p class="text-gray-300 text-lg mb-10">
          Partner with NK Technologies for integrated engineering solutions that deliver results. 
          Let's discuss how we can bring your vision to life.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a 
            href="/contact" 
            class="px-8 py-4 bg-gradient-to-r from-[#ED7D31] to-orange-600 text-white font-semibold rounded-lg hover:shadow-lg hover:shadow-[#ED7D31]/50 transition-all transform hover:scale-105"
          >
            Start a Conversation
          </a>
          
          <a 
            href="tel:+919730553516" 
            class="px-8 py-4 bg-white/10 backdrop-blur-sm text-white font-semibold rounded-lg border border-white/20 hover:bg-white/20 transition-all transform hover:scale-105"
          >
            Call +91-97305 53516
          </a>
        </div>
      </div>
    </div>
  </section>


</div>
