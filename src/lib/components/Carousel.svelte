<script lang="ts">
  const images = [
    "/generated/image-beautiful-completed-pool-with-natural-st-1765587811454-2.webp",
    "/generated/image-elegant-outdoor-living-space-with-pergol-1765587814506-3.webp",
    "/generated/image-modern-landscape-design-with-terraced-ga-1765587817132-4.webp"
  ];
</script>

<section class="bg-white pb-24 overflow-hidden">
  <div class="flex gap-4 overflow-x-auto px-6 pb-8 snap-x">
    {#each images as img}
      <div class="min-w-[80vw] md:min-w-[60vw] lg:min-w-[45vw] h-[400px] snap-center first:pl-0">
        <img src={img} alt="Completed project" class="w-full h-full object-cover rounded-lg" />
      </div>
    {/each}
  </div>
  
  <div class="text-center mt-4">
    <p class="text-gray-500 text-sm mb-4">Recent Projects <span class="text-gray-400">Pools • Landscapes • Outdoor Living</span></p>
    <div class="flex justify-center gap-2">
      <div class="w-1.5 h-1.5 rounded-full bg-gray-800"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
    </div>
  </div>
</section>
