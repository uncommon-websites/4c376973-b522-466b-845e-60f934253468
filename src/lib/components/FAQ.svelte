<script lang="ts">
  import { Plus } from 'lucide-svelte';

  const faqs = [
    "Can I add training after I complete my registration?",
    "How do group passes work?",
    "Do you have a justification letter to help persuade my organization to sponsor my attendance?",
    "Can I request an accessibility accommodation to attend the event?",
    "Is there a minimum age requirement to attend?",
    "How can I book a room at one of the Sessions hotels?",
    "Can I transfer my ticket to someone else?",
    "Can I modify or cancel my registration?",
    "Can I modify or cancel my training pass?",
    "I have additional questions that weren't covered here. Who can I contact?"
  ];
</script>

<section class="py-20 px-6 max-w-[1400px] mx-auto border-t border-gray-200" id="faq">
  <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-4">
      <h2 class="text-[clamp(2.5rem,5vw,4rem)] leading-none font-medium text-[#110F28]">FAQs</h2>
    </div>

    <div class="lg:col-span-8">
      <div class="border-t border-gray-200">
        {#each faqs as question}
          <div class="py-5 border-b border-gray-200 flex justify-between items-center cursor-pointer group hover:bg-gray-50 transition-colors px-2 -mx-2 rounded-sm">
            <h3 class="text-sm font-medium text-[#110F28] pr-8">{question}</h3>
            <div class="text-gray-400 group-hover:text-[#110F28] transition-colors">
              <Plus size={16} />
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
