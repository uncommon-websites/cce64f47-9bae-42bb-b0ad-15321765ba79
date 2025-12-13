<script lang="ts">
  export let text = "Get Started";
  export let href = "#contact";
</script>

<div class="bg-black text-white text-[11px] font-medium py-3 px-4 flex justify-between items-center tracking-wide">
  <div class="flex-1 text-center">
    <span class="opacity-90">Transform your high-value construction project with expert oversight</span>
  </div>
  <a {href} class="bg-primary-600 hover:bg-primary-700 text-white px-3 py-1.5 rounded text-[10px] font-bold uppercase tracking-wider ml-4 transition-colors">
    {text}
  </a>
</div>
