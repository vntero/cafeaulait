<script>
  import KurseCard from './KurseCard.svelte'
  import SectionWrapper from './SectionWrapper.svelte'
  import { onMount, onDestroy } from 'svelte'
  let kurseFeatures = [
    {
      featureList: [
        'Afrotanz als Sport & Bewegung',
        'Afrobeats',
        'CAL Gospechor',
        'CAL Stage Company',
      ],
      description: '',
      imgUrl: 'assets/afrotanz.png',
    },
  ]

  let currentIndex = 0
  let intervalId

  onMount(() => {
    intervalId = setInterval(() => {
      currentIndex = (currentIndex + 1) % kurseFeatures.length
    }, 2000)
  })

  onDestroy(() => clearInterval(intervalId))
</script>

<SectionWrapper id="kurse">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Kurse
      </h3>
    </div>
    {#each kurseFeatures as kurseFeature, index}
      <KurseCard {kurseFeature} {index}>
        {#if index === 0}
          Unsere Tanz-, Trommel und Gesangskurse – <span
            class="text-red-500 font-medium"
          >
            ab 6 Jahren</span
          >
        {/if}
      </KurseCard>
    {/each}
  </div>
</SectionWrapper>
