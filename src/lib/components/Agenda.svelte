<script lang="ts">
  import AgendaItem from './AgendaItem.svelte';

  const day1 = {
    date: "April 28",
    tags: ["Pre-event"],
    items: [
      { time: "All day", title: "Pre-conference training (add-on)", subtitle: "Partner Summit (for Stripe partners only)" }
    ]
  };

  const day2 = {
    date: "April 29",
    tags: ["Day 1"],
    items: [
      { time: "Morning", content: ["Breakfast in the expo hall", "Keynote", "Breakout talks", "Hands-on workrooms", "Certification exams"] },
      { time: "Afternoon", content: ["Lunch at Yerba Buena Gardens", "Expo hall", "Breakout talks", "Hands-on workrooms", "Certification exams", "Fireside chat with special guest"] },
      { time: "Evening", title: "Welcome reception" }
    ]
  };

  const day3 = {
    date: "April 30",
    tags: ["Day 2"],
    items: [
      { time: "Morning", content: ["Breakfast in the expo hall", "Keynote", "Breakout talks", "Hands-on workrooms", "Certification exams"] },
      { time: "Afternoon", content: ["Lunch at Yerba Buena Gardens", "Expo hall", "Breakout talks", "Hands-on workrooms", "Certification exams", "Fireside chat with special guest"] },
      { time: "Evening", title: "Networking hour" }
    ]
  };
</script>

<section class="px-6 max-w-[1400px] mx-auto">
  <AgendaItem {...day1} />
  <AgendaItem {...day2} />
  <AgendaItem {...day3} />
</section>
