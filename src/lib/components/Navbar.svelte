<script lang="ts">
  import { page } from '$app/stores';
</script>

<nav class="bg-black text-white py-4 px-6 flex items-center justify-between sticky top-0 z-50 border-b border-gray-900">
  <div class="flex items-center gap-8">
    <a href="/" class="text-2xl font-medium tracking-tight">Solid Plan</a>
    
    <div class="hidden md:flex items-center gap-6 text-[13px] font-medium text-gray-300">
      <a href="#services" class="hover:text-white transition-colors">Services</a>
      <a href="#process" class="hover:text-white transition-colors">Our Process</a>
      <a href="#projects" class="hover:text-white transition-colors">Projects</a>
      <a href="#about" class="hover:text-white transition-colors">About</a>
    </div>
  </div>

  <div class="flex items-center gap-4">
    <a href="#contact" class="bg-primary-600 hover:bg-primary-700 text-white px-4 py-2 rounded-full text-[13px] font-medium transition-colors">
      Start Your Project
    </a>
  </div>
</nav>
