<script lang="ts">
  import { ArrowLeft, ArrowRight } from 'lucide-svelte';

  const featuredSpeakers = [
    { name: 'Patrick Collison', role: 'Stripe Co-founder and CEO', img: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=300&q=80' },
    { name: 'John Collison', role: 'Stripe Co-founder and President', img: 'https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=300&q=80' },
    { name: 'Will Gaybrick', role: 'Stripe President, Technology and Business', img: 'https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?auto=format&fit=crop&w=300&q=80' },
    { name: 'Eileen O\'Mara', role: 'Stripe Chief Revenue Officer', img: 'https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&w=300&q=80' }
  ];

  const moreSpeakers = [
    { name: 'Michelle Bu', role: 'Head of Developer Experience and Product Platform', company: 'Stripe' },
    { name: 'Dan Chandre', role: 'SVP, Commercial', company: 'Squarespace' },
    { name: 'Curtis Crawford', role: 'Director and GM, Fintech and Loyalty Organization', company: 'Wayfair' },
    { name: 'Tanya Khakbaz', role: 'Head of Product Marketing', company: 'Stripe' },
    { name: 'Ara Kharazian', role: 'Economist', company: 'Ramp' },
    { name: 'Emily Sands', role: 'Head of Information', company: 'Stripe' },
    { name: 'Henri Stern', role: 'CEO', company: 'Privy' },
    { name: 'Tony Vardiman', role: 'VP, Global Payments and Operations', company: 'Cloudbeds' }
  ];
</script>

<section class="py-20 px-6 max-w-[1400px] mx-auto border-t border-gray-200 overflow-hidden">
  <h2 class="text-[clamp(2.5rem,5vw,4rem)] leading-none font-medium mb-8 text-[#110F28]">Speakers</h2>
  
  <p class="text-sm font-medium text-gray-600 mb-6">Featured</p>

  <!-- Carousel (Simplified as grid for now, but styled to look like carousel) -->
  <div class="relative w-full overflow-x-auto pb-12 hide-scrollbar">
    <div class="flex gap-6 min-w-max">
      {#each featuredSpeakers as speaker}
        <div class="w-[280px] md:w-[320px] bg-white rounded-lg overflow-hidden shadow-sm group cursor-pointer relative flex flex-col h-[420px] border border-gray-100 transition-all hover:shadow-md">
            <!-- Top Section with Name and Image -->
            <div class="relative flex-grow bg-gray-50 overflow-hidden">
                <!-- Name -->
                <div class="absolute top-6 left-6 z-10">
                    <h3 class="text-3xl font-medium text-[#110F28] leading-[0.9] tracking-tight">
                        {#each speaker.name.split(' ') as word}
                            <div>{word}</div>
                        {/each}
                    </h3>
                </div>
                
                <!-- Image -->
                <img 
                    src={speaker.img} 
                    alt={speaker.name} 
                    class="absolute bottom-0 right-0 w-[85%] h-auto object-cover object-bottom grayscale group-hover:grayscale-0 transition-all duration-500 mix-blend-multiply" 
                />
            </div>

            <!-- Bottom Section with Role -->
            <div class="p-6 bg-white border-t border-gray-100 relative">
                <p class="text-xs font-bold text-[#110F28] mb-1">Stripe</p>
                <p class="text-xs text-gray-600">{speaker.role.replace('Stripe ', '')}</p>
                
                <!-- Arrow Icon -->
                <div class="absolute bottom-6 right-6 opacity-0 group-hover:opacity-100 transition-opacity">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-[#110F28]"><path d="M7 17L17 7"></path><path d="M7 7h10v10"></path></svg>
                </div>
            </div>
        </div>
      {/each}
    </div>
  </div>

  <!-- Navigation Buttons -->
  <div class="flex justify-between items-center mb-16">
    <button class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center text-gray-600 hover:bg-gray-200 transition-colors">
      <ArrowLeft size={16} />
    </button>
    <button class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center text-gray-600 hover:bg-gray-200 transition-colors">
      <ArrowRight size={16} />
    </button>
  </div>

  <!-- More Speakers List -->
  <div>
    <p class="text-sm font-medium text-gray-600 mb-6">More speakers</p>
    <div class="border-t border-gray-200">
      {#each moreSpeakers as speaker}
        <div class="grid grid-cols-1 md:grid-cols-12 py-4 border-b border-gray-200 items-center hover:bg-gray-50 transition-colors cursor-pointer group">
          <div class="md:col-span-4">
            <h3 class="text-xl font-normal text-[#110F28]">{speaker.name}</h3>
          </div>
          <div class="md:col-span-7">
            <p class="text-xs font-bold text-[#110F28] mb-0.5">{speaker.company}</p>
            <p class="text-xs text-gray-600">{speaker.role}</p>
          </div>
          <div class="md:col-span-1 flex justify-end opacity-0 group-hover:opacity-100 transition-opacity">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-gray-400"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
          </div>
        </div>
      {/each}
    </div>
    <p class="text-sm text-gray-500 mt-8">Stay tuned for more speaker announcements.</p>
  </div>

</section>

<style>
  .hide-scrollbar::-webkit-scrollbar {
    display: none;
  }
  .hide-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
</style>
