<script>
  import { onMount } from 'svelte';
  import LoadingSpinner from '$lib/components/LoadingSpinner.svelte';
  import SEO from '$lib/components/SEO.svelte';
  
  let mounted = false;
  let formData = {
    name: '',
    email: '',
    phone: '',
    company: '',
    subject: '',
    message: ''
  };
  
  let formStatus = { type: '', message: '' };
  let isSubmitting = false;
  
  onMount(() => {
    mounted = true;
  });
  
  async function handleSubmit(e) {
    e.preventDefault();
    isSubmitting = true;
    formStatus = { type: '', message: '' };
    
    try {
      // Simulate a slight delay to show the spinner
      await new Promise(resolve => setTimeout(resolve, 500));
      
      // Create mailto link with form data
      const subject = encodeURIComponent(formData.subject || 'Contact Form Submission');
      const body = encodeURIComponent(
        `Name: ${formData.name}\n` +
        `Email: ${formData.email}\n` +
        `Phone: ${formData.phone}\n` +
        `Company: ${formData.company}\n\n` +
        `Message:\n${formData.message}`
      );
      
      const mailtoLink = `mailto:karan@nk-technologies.com?subject=${subject}&body=${body}`;
      window.location.href = mailtoLink;
      
      formStatus = {
        type: 'success',
        message: 'Your email client should open now. Please send the message.'
      };
      
      // Reset form after a delay
      setTimeout(() => {
        formData = {
          name: '',
          email: '',
          phone: '',
          company: '',
          subject: '',
          message: ''
        };
      }, 1000);
      
    } catch (error) {
      formStatus = {
        type: 'error',
        message: 'Something went wrong. Please try again or contact us directly.'
      };
    } finally {
      isSubmitting = false;
    }
  }
</script>

<SEO 
  title="Contact NK Technologies - Get Engineering Solutions Quote"
  description="Contact NK Technologies for engineering solutions. Located in Pune, Maharashtra. Call +91-97305 53516 or email karan@nk-technologies.com for expert consultation."
  keywords="contact NK Technologies, engineering solutions pune, get quote, consultation, Ambegaon Budruk Pune"
  ogImage="/og-contact.jpg"
/>


<svelte:head>
  <title>NK Technologies || Contact</title>
</svelte:head>

<div class="min-h-screen bg-[#100A40] text-white">
  <!-- Hero Section -->
  <section class="relative overflow-hidden pt-24 pb-12">
    <div class="absolute inset-0 opacity-10">
      <div class="absolute inset-0 bg-gradient-to-br from-[#ED7D31] via-transparent to-transparent"></div>
    </div>
    
    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center max-w-4xl mx-auto">
        <p class="text-[#ED7D31] text-sm font-semibold tracking-wider mb-4">GET IN TOUCH</p>
        <h1 class="text-5xl md:text-7xl font-bold mb-6 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
          Contact Us
        </h1>
        <p class="text-lg text-gray-300">
          Ready to transform your engineering challenges into success stories? 
          Let's start a conversation about your project.
        </p>
      </div>
    </div>
  </section>

  <!-- Contact Form & Info Section -->
  <section class="py-16">
    <div class="container mx-auto px-6">
      <div class="grid lg:grid-cols-2 gap-12">
        <!-- Contact Form -->
        <div class="order-2 lg:order-1" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out;">
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10">
            <h2 class="text-3xl font-bold mb-6">Send us a Message</h2>
            
            {#if formStatus.message}
              <div class="mb-6 p-4 rounded-lg {formStatus.type === 'success' ? 'bg-green-500/20 border border-green-500/50' : 'bg-red-500/20 border border-red-500/50'}">
                <p class="text-sm">{formStatus.message}</p>
              </div>
            {/if}
            
            <form on:submit={handleSubmit} class="space-y-6">
  <div class="grid md:grid-cols-2 gap-6">
    <div>
      <label for="name" class="block text-sm font-medium mb-2">
        Name <span class="text-[#ED7D31]">*</span>
      </label>
      <input
        type="text"
        id="name"
        name="name"
        bind:value={formData.name}
        required
        aria-required="true"
        class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:border-[#ED7D31] transition-colors text-white placeholder-gray-400"
        placeholder="Your full name"
      />
    </div>
    
    <div>
      <label for="email" class="block text-sm font-medium mb-2">
        Email <span class="text-[#ED7D31]">*</span>
      </label>
      <input
        type="email"
        id="email"
        name="email"
        bind:value={formData.email}
        required
        aria-required="true"
        class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:border-[#ED7D31] transition-colors text-white placeholder-gray-400"
        placeholder="your@email.com"
      />
    </div>
  </div>
  
  <div class="grid md:grid-cols-2 gap-6">
    <div>
      <label for="phone" class="block text-sm font-medium mb-2">Phone</label>
      <input
        type="tel"
        id="phone"
        name="phone"
        bind:value={formData.phone}
        class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:border-[#ED7D31] transition-colors text-white placeholder-gray-400"
        placeholder="+91 98765 43210"
      />
    </div>
    
    <div>
      <label for="company" class="block text-sm font-medium mb-2">Company</label>
      <input
        type="text"
        id="company"
        name="company"
        bind:value={formData.company}
        class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:border-[#ED7D31] transition-colors text-white placeholder-gray-400"
        placeholder="Your company name"
      />
    </div>
  </div>
  
  <div>
    <label for="subject" class="block text-sm font-medium mb-2">
      Subject <span class="text-[#ED7D31]">*</span>
    </label>
    <input
      type="text"
      id="subject"
      name="subject"
      bind:value={formData.subject}
      required
      aria-required="true"
      class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:border-[#ED7D31] transition-colors text-white placeholder-gray-400"
      placeholder="How can we help you?"
    />
  </div>
  
  <div>
    <label for="message" class="block text-sm font-medium mb-2">
      Message <span class="text-[#ED7D31]">*</span>
    </label>
    <textarea
      id="message"
      name="message"
      bind:value={formData.message}
      required
      aria-required="true"
      rows="6"
      class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:border-[#ED7D31] transition-colors text-white placeholder-gray-400 resize-none"
      placeholder="Tell us about your project requirements..."
    ></textarea>
  </div>
  
  <button
    type="submit"
    disabled={isSubmitting}
    aria-busy={isSubmitting}
    class="w-full px-8 py-4 bg-gradient-to-r from-[#ED7D31] to-orange-600 text-white font-semibold rounded-lg 
           hover:shadow-lg hover:shadow-[#ED7D31]/50 transition-all transform hover:scale-105 
           disabled:opacity-50 disabled:cursor-not-allowed disabled:hover:scale-100 disabled:hover:shadow-none
           flex items-center justify-center gap-2"
  >
    {#if isSubmitting}
      <LoadingSpinner size="sm" color="#ffffff" />
      <span>Sending Message...</span>
    {:else}
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"/>
      </svg>
      <span>Send Message</span>
    {/if}
  </button>
</form>

          </div>
        </div>


        <!-- Contact Information -->
        <div class="order-1 lg:order-2 space-y-6" class:opacity-0={!mounted} class:translate-y-8={!mounted} 
             class:opacity-100={mounted} class:translate-y-0={mounted} 
             style="transition: all 0.8s ease-out 0.2s;">
          
          <div class="bg-gradient-to-br from-white/10 to-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10">
            <h2 class="text-3xl font-bold mb-6">Get in Touch</h2>
            <p class="text-gray-300 mb-8">
              Have a question or want to discuss a project? We're here to help. 
              Reach out to us through any of the following channels.
            </p>
            
            <!-- Phone -->
            <div class="flex items-start gap-4 mb-6 group">
              <div class="w-12 h-12 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center flex-shrink-0 group-hover:scale-110 transition-transform">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                </svg>
              </div>
              <div>
                <h3 class="font-semibold text-lg mb-1">Phone</h3>
                <a href="tel:+919730553516" class="text-gray-300 hover:text-[#ED7D31] transition-colors">
                  +91-97305 53516
                </a>
              </div>
            </div>
            
            <!-- Email -->
            <div class="flex items-start gap-4 mb-6 group">
              <div class="w-12 h-12 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center flex-shrink-0 group-hover:scale-110 transition-transform">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                </svg>
              </div>
              <div>
                <h3 class="font-semibold text-lg mb-1">Email</h3>
                <a href="mailto:karan@nk-technologies.com" class="text-gray-300 hover:text-[#ED7D31] transition-colors">
                  karan@nk-technologies.com
                </a>
              </div>
            </div>
            
            <!-- Address -->
            <div class="flex items-start gap-4 group">
              <div class="w-12 h-12 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-lg flex items-center justify-center flex-shrink-0 group-hover:scale-110 transition-transform">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
              </div>
              <div>
                <h3 class="font-semibold text-lg mb-1">Office Address</h3>
                <p class="text-gray-300">
                  Near Katraj-Dehu Rd Bypass, C'Lai World,<br />
                  opp. Podar International School,<br />
                  Ambegaon Budruk, Pune,<br />
                  Maharashtra 411046
                </p>
              </div>
            </div>
          </div>
          
          <!-- Business Hours -->
          <div class="bg-gradient-to-br from-white/10 to-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10">
            <h3 class="text-xl font-bold mb-4">Business Hours</h3>
            <div class="space-y-3">
              <div class="flex justify-between">
                <span class="text-gray-300">Monday - Friday</span>
                <span class="font-semibold">9:00 AM - 6:00 PM</span>
              </div>
              <div class="flex justify-between">
                <span class="text-gray-300">Saturday</span>
                <span class="font-semibold">9:00 AM - 2:00 PM</span>
              </div>
              <div class="flex justify-between">
                <span class="text-gray-300">Sunday</span>
                <span class="font-semibold text-gray-500">Closed</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>


 <!-- Map Section -->
  <section class="py-16 bg-gradient-to-b from-transparent to-white/5">
    <div class="container mx-auto px-6">
      <div class="text-center mb-12">
        <h2 class="text-4xl font-bold mb-4 bg-gradient-to-r from-[#ED7D31] via-orange-400 to-[#ED7D31] bg-clip-text text-transparent">
          Find Us Here
        </h2>
        <p class="text-gray-300">
          Visit our office in Pune for a detailed discussion about your engineering needs
        </p>
      </div>
      
      <div class="rounded-2xl overflow-hidden shadow-2xl border border-white/10">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3784.7523456789!2d73.8567!3d18.4647!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMTjCsDI3JzUyLjkiTiA3M8KwNTEnMjQuMSJF!5e0!3m2!1sen!2sin!4v1234567890"
          width="100%"
          height="450"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          title="NK Technologies Location"
        ></iframe>
      </div>
    </div>
  </section>

  <!-- Why Choose Us Quick Section -->
  <section class="py-16">
    <div class="container mx-auto px-6">
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 text-center hover:border-[#ED7D31]/50 transition-all">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-full flex items-center justify-center mx-auto mb-4">
            <span class="text-3xl">⚡</span>
          </div>
          <h3 class="text-xl font-bold mb-2">Quick Response</h3>
          <p class="text-gray-400 text-sm">
            We respond to all inquiries within 24 hours
          </p>
        </div>
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 text-center hover:border-[#ED7D31]/50 transition-all">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-full flex items-center justify-center mx-auto mb-4">
            <span class="text-3xl">🎯</span>
          </div>
          <h3 class="text-xl font-bold mb-2">Expert Consultation</h3>
          <p class="text-gray-400 text-sm">
            Free initial consultation with our engineering experts
          </p>
        </div>
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 text-center hover:border-[#ED7D31]/50 transition-all">
          <div class="w-16 h-16 bg-gradient-to-br from-[#ED7D31] to-orange-600 rounded-full flex items-center justify-center mx-auto mb-4">
            <span class="text-3xl">🤝</span>
          </div>
          <h3 class="text-xl font-bold mb-2">Tailored Solutions</h3>
          <p class="text-gray-400 text-sm">
            Custom solutions designed for your specific needs
          </p>
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
          Let's Build Something Great Together
        </h2>
        
        <p class="text-gray-300 text-lg mb-10">
          Whether you have a question about our services, need a quote, or want to discuss a project, 
          our team is ready to answer all your questions.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a 
            href="tel:+919730553516" 
            class="px-8 py-4 bg-gradient-to-r from-[#ED7D31] to-orange-600 text-white font-semibold rounded-lg hover:shadow-lg hover:shadow-[#ED7D31]/50 transition-all transform hover:scale-105 flex items-center justify-center gap-2"
          >
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
            </svg>
            Call Now: +91-97305 53516
          </a>
          
          <a 
            href="mailto:karan@nk-technologies.com" 
            class="px-8 py-4 bg-white/10 backdrop-blur-sm text-white font-semibold rounded-lg border border-white/20 hover:bg-white/20 transition-all transform hover:scale-105 flex items-center justify-center gap-2"
          >
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
            </svg>
            Email Us
          </a>
        </div>
        
        <div class="mt-12 pt-8 border-t border-white/10">
          <p class="text-gray-400 mb-4">Or explore more about us</p>
          <div class="flex flex-wrap justify-center gap-4">
            <a 
              href="/about" 
              class="text-[#ED7D31] hover:text-orange-400 transition-colors font-medium"
            >
              About Us →
            </a>
            <span class="text-gray-600">|</span>
            <a 
              href="/services" 
              class="text-[#ED7D31] hover:text-orange-400 transition-colors font-medium"
            >
              Our Services →
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>