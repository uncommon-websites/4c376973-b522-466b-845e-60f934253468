<section class="py-20 px-6 max-w-[1400px] mx-auto border-t border-gray-200">
  <h2 class="text-[clamp(2.5rem,5vw,4rem)] leading-none font-medium mb-16 text-[#110F28]">Conference passes</h2>

  <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
    <!-- Cards -->
    <div class="lg:col-span-8 grid grid-cols-1 md:grid-cols-2 gap-6">
      
      <!-- Card 1 -->
      <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 flex flex-col h-full relative overflow-hidden group hover:shadow-md transition-shadow">
        <div class="flex justify-between items-start mb-6">
          <h3 class="text-sm font-medium text-gray-900">Conference pass</h3>
          <span class="bg-gray-100 text-gray-600 text-[10px] uppercase tracking-wider font-semibold px-2 py-1 rounded">Early bird</span>
        </div>
        
        <div class="flex items-baseline gap-2 mb-8">
          <span class="text-4xl font-medium text-[#110F28]">$599</span>
          <span class="text-gray-400 line-through text-sm">$899</span>
        </div>

        <p class="text-sm text-gray-600 mb-8 flex-grow">
          Get an additional $200 off each pass when you purchase 5 or more passes.
        </p>

        <div class="mt-auto">
          <p class="text-xs text-gray-500 mb-4">Save with early-bird rates through January 31, 2026.</p>
          <button class="w-full bg-[#110F28] text-white py-3 rounded-full text-sm font-medium hover:bg-opacity-90 transition-opacity">Register</button>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 flex flex-col h-full relative overflow-hidden group hover:shadow-md transition-shadow">
        <div class="flex justify-between items-start mb-6">
          <h3 class="text-sm font-medium text-gray-900">Conference pass + training bundle</h3>
          <span class="bg-gray-100 text-gray-600 text-[10px] uppercase tracking-wider font-semibold px-2 py-1 rounded">Early bird</span>
        </div>
        
        <div class="flex items-baseline gap-2 mb-8">
          <span class="text-4xl font-medium text-[#110F28]">$799</span>
        </div>

        <p class="text-sm text-gray-600 mb-8 flex-grow">
          Get training for $200 ($399 value) when you purchase a conference pass.
        </p>

        <div class="mt-auto">
          <p class="text-xs text-gray-500 mb-4">Offer excludes other discounts and registration codes.</p>
          <button class="w-full bg-[#110F28] text-white py-3 rounded-full text-sm font-medium hover:bg-opacity-90 transition-opacity">Register</button>
        </div>
      </div>

    </div>

    <!-- Included List -->
    <div class="lg:col-span-4 pl-0 lg:pl-12 pt-4">
      <h3 class="text-sm font-medium text-[#110F28] mb-6">What's included</h3>
      <ul class="space-y-4">
        {#each ['Keynotes', 'Breakout talks', 'Expo hall', 'Meals', 'Networking opportunities', 'Evening events', 'Stripe merch'] as item}
          <li class="text-sm text-gray-600 flex items-center gap-3">
             {item}
          </li>
        {/each}
      </ul>
    </div>
  </div>
</section>
