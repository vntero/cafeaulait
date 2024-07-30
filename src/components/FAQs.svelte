<script>
  import SectionWrapper from './SectionWrapper.svelte'
  let faqs = [
    {
      question: 'Unser Nachwuchs',
      ans: 'Swoley Moley is a fun fitness app designed to make your workouts enjoyable by incorporating interactive games and challenges.',
    },
    {
      question: 'Unsere Künstler',
      ans: 'You can download Swoley Moley from the App Store (for iOS) or Google Play Store (for Android) on your mobile device.',
    },
    {
      question: 'Unser Team',
      ans: 'Yes, Swoley Moley offers a free version with basic features. There is also a premium subscription that unlocks additional games and advanced workout tracking.',
    },
  ]
</script>

<SectionWrapper id="faqs">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <br />
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Ein Einblick in unsere <span class="text-red-500">Welt</span>
      </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">
            {faq.question}
          </h4>
          <p class="pl-2">{faq.ans}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
