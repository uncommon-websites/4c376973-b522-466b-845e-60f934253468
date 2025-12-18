<script lang="ts">
  import { Pause, Volume2 } from 'lucide-svelte';
</script>

<section class="py-20 px-6 max-w-[1400px] mx-auto border-t border-gray-200">
  <h2 class="text-[clamp(2.5rem,5vw,4rem)] leading-none font-medium mb-16 text-[#110F28]">Why attend</h2>

  <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
    <!-- Left Content -->
    <div class="lg:col-span-5 flex flex-col gap-16">
      
      <!-- Item 1 -->
      <div>
        <h3 class="text-xl font-medium mb-3 text-[#110F28]">See what's next in payments and commerce</h3>
        <p class="text-sm leading-relaxed text-gray-600">
          Head to the main stage to see our biggest product announcements live, hear from renowned business leaders, and explore what's next for global commerce as AI-native models, agentic commerce, and crypto reshape how business gets done.
        </p>
      </div>

      <!-- Item 2 -->
      <div>
        <h3 class="text-xl font-medium mb-3 text-[#110F28]">Learn how to meet the trends impacting your business</h3>
        <p class="text-sm leading-relaxed text-gray-600 mb-4">
          Build your own agenda of breakout talks covering the next wave of revenue models, AI-powered payment optimizations, designing exceptional customer experiences, and more. Whether you're a newcomer or experienced practitioner, you'll find talks that match your expertise.
        </p>
      </div>

      <!-- Item 3 -->
      <div>
        <h3 class="text-xl font-medium mb-3 text-[#110F28]">Expand your skills with training and certification</h3>
        <p class="text-sm leading-relaxed text-gray-600 mb-3">Topics:</p>
        <ul class="list-disc pl-5 text-sm leading-relaxed text-gray-600 space-y-1 mb-4">
          <li>Increasing conversion and lowering network costs</li>
          <li>Fighting fraud and managing disputes</li>
          <li>Building your recurring revenue engine</li>
          <li>Establishing your vertical SaaS platform</li>
          <li>Increasing the global reach of your business with stablecoins</li>
          <li>Developing an AI agent-ready checkout experience</li>
        </ul>
        <p class="text-sm leading-relaxed text-gray-600">
          Included: On-site certification exams and hands-on workrooms (Wednesday and Thursday)
        </p>
      </div>

      <!-- Training Box -->
      <div class="bg-gray-100 p-4 rounded-lg flex items-center justify-between group cursor-pointer hover:bg-gray-200 transition-colors">
        <div>
          <p class="text-xs font-medium text-[#110F28]">Add training to your</p>
          <p class="text-xs font-medium text-[#110F28]">conference pass at checkout.</p>
          <p class="text-xs text-[#635bff] mt-1 group-hover:underline">Learn more</p>
        </div>
        <div class="w-6 h-6 rounded-full bg-gray-300 flex items-center justify-center">
            <svg width="10" height="10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-gray-600"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
        </div>
      </div>

      <hr class="border-gray-200" />

      <!-- Item 4 -->
      <div>
        <h3 class="text-xl font-medium mb-3 text-[#110F28]">Make new connections in the expo hall</h3>
        <p class="text-sm leading-relaxed text-gray-600">
          Meet our partners and discover tools that extend Stripe's capabilities through demos and talks. Between sessions, join focused meetups to share ideas with peers, find opportunities to solve business challenges, and connect with the Stripe community that supports you year-round.
        </p>
      </div>

    </div>

    <!-- Right Content (Visual) -->
    <div class="lg:col-span-7 relative min-h-[600px] bg-[#110F28] rounded-sm overflow-hidden">
      <!-- Placeholder for abstract visual/video -->
      <div class="absolute inset-0 bg-gradient-to-br from-[#110F28] to-[#2E1153]"></div>
      
      <!-- Controls -->
      <div class="absolute bottom-6 right-6 flex gap-2">
        <button class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md flex items-center justify-center text-white hover:bg-white/20 transition-colors">
          <Pause size={16} />
        </button>
        <button class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md flex items-center justify-center text-white hover:bg-white/20 transition-colors">
          <Volume2 size={16} />
        </button>
      </div>
    </div>
  </div>
</section>
