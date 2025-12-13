<script lang="ts">
  let selectedTier = 'growth';
  
  const tiers = [
    {
      id: 'essentials',
      name: 'Essentials',
      tagline: 'Perfect for smaller projects',
      features: ['2-hour deep-dive session', 'Biological systems review', 'Follow-up report', '2 weeks email support'],
      ideal: 'Single-phase projects'
    },
    {
      id: 'growth',
      name: 'Growth',
      tagline: 'Most popular for complex builds',
      features: ['5-hour strategy workshop', 'Full biological systems assessment', 'Custom strategic roadmap', '3 months priority email support'],
      ideal: 'Multi-phase landscapes'
    },
    {
      id: 'enterprise',
      name: 'Enterprise',
      tagline: 'Complete oversight & management',
      features: ['Full biological systems audit', 'Custom multi-phase business plan', 'On-site consulting and team training', '24/7 premium support'],
      ideal: 'Estate-level projects'
    }
  ];
  
  $: currentTier = tiers.find(t => t.id === selectedTier) || tiers[1];
</script>

<section class="bg-[#f9f9f7] py-24 px-6" id="services">
  <div class="max-w-[1200px] mx-auto text-center">
    <h2 class="text-[40px] font-light text-gray-900 mb-16">
      Three service tiers. <span class="text-gray-400">Tailored to your project.</span>
    </h2>

    <div class="mb-8">
      <h3 class="text-2xl font-normal mb-2">{currentTier.name}</h3>
      <p class="text-gray-500 text-sm">{currentTier.tagline}</p>
    </div>

    <!-- Service Tier Display -->
    <div class="relative w-full min-h-[400px] bg-white rounded-xl mb-8 flex items-center justify-center overflow-hidden shadow-sm p-12">
      <div class="max-w-[600px]">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-8">
          {#each currentTier.features as feature}
            <div class="flex items-start gap-2 text-left">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-primary-600 flex-shrink-0 mt-0.5"><path d="M20 6L9 17l-5-5"/></svg>
              <span class="text-sm text-gray-700">{feature}</span>
            </div>
          {/each}
        </div>
        
        <div class="bg-gray-50 rounded-lg p-4 text-center">
          <p class="text-xs text-gray-500 mb-1">Ideal for</p>
          <p class="text-base font-medium text-gray-900">{currentTier.ideal}</p>
        </div>
      </div>
    </div>

    <!-- Tier Selector -->
    <div class="flex justify-center gap-4 mb-8">
      {#each tiers as tier}
        <button 
          on:click={() => selectedTier = tier.id}
          class="px-6 py-3 rounded-lg text-sm font-medium transition-all {selectedTier === tier.id ? 'bg-primary-600 text-white' : 'bg-white text-gray-700 hover:bg-gray-100'}"
        >
          {tier.name}
        </button>
      {/each}
    </div>

    <div class="flex justify-center gap-4">
      <button class="px-6 py-3 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors">
        Schedule Consultation
      </button>
      <button class="px-6 py-3 bg-white hover:bg-gray-100 border border-gray-200 rounded-lg text-sm font-medium transition-colors">
        Compare All Tiers
      </button>
    </div>
  </div>
</section>
