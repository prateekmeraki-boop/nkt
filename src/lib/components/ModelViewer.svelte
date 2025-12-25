<script>
  import { onMount } from 'svelte';
  import * as THREE from 'three';
  import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js';
  import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls.js';
  
  let container;
  
  onMount(() => {
    const scene = new THREE.Scene();
    
    // Adjust aspect ratio and camera
    const camera = new THREE.PerspectiveCamera(45, 1, 0.1, 1000); // Changed FOV from 75 to 45
    camera.position.set(0, 2, 8); // Adjusted camera position
    
    const renderer = new THREE.WebGLRenderer({ 
      alpha: true, 
      antialias: true 
    });
    
    // Make sure renderer takes full container size
    const updateSize = () => {
      const width = container.clientWidth;
      const height = container.clientHeight;
      renderer.setSize(width, height);
      camera.aspect = width / height;
      camera.updateProjectionMatrix();
    };
    
    updateSize();
    container.appendChild(renderer.domElement);
    
    // Lighting
    const ambientLight = new THREE.AmbientLight(0xffffff, 0.8);
    scene.add(ambientLight);
    
    const directionalLight = new THREE.DirectionalLight(0xffffff, 1.2);
    directionalLight.position.set(5, 5, 5);
    scene.add(directionalLight);
    
    // Load model
    const loader = new GLTFLoader();
    loader.load('/models/scene.gltf', (gltf) => {
      const model = gltf.scene;
      
      // Center and scale the model
      const box = new THREE.Box3().setFromObject(model);
      const center = box.getCenter(new THREE.Vector3());
      const size = box.getSize(new THREE.Vector3());
      
      // Scale model to fit view
      const maxDim = Math.max(size.x, size.y, size.z);
      const scale = 4 / maxDim; // Adjust this value to change model size
      model.scale.multiplyScalar(scale);
      
      // Center the model
      model.position.sub(center.multiplyScalar(scale));
      
      scene.add(model);
    });
    
    // Controls
    const controls = new OrbitControls(camera, renderer.domElement);
    controls.enableDamping = true;
    controls.dampingFactor = 0.05;
    controls.autoRotate = true;
    controls.autoRotateSpeed = 1;
    controls.enableZoom = false; // Disable zoom to prevent cropping issues
    controls.minPolarAngle = Math.PI / 4;
    controls.maxPolarAngle = Math.PI / 1.5;
    
    // Animation loop
    function animate() {
      requestAnimationFrame(animate);
      controls.update();
      renderer.render(scene, camera);
    }
    animate();
    
    // Handle window resize
    window.addEventListener('resize', updateSize);
    
    // Cleanup
    return () => {
      window.removeEventListener('resize', updateSize);
      renderer.dispose();
      controls.dispose();
    };
  });
</script>

<div bind:this={container} class="w-full h-full"></div>
