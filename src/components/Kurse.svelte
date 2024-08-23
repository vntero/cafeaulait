<script>
  import KurseCard from './KurseCard.svelte'
  import SectionWrapper from './SectionWrapper.svelte'
  let kurseFeatures = [
    {
      featureList: [
        'Traditional',
        'Original',
        'Renowned teachers',
        'Percussion',
      ],
      description:
        'Komplexe panafrikanische Tänze werden auf mittlerem bis fortgeschrittenem Niveau erarbeitet.',
      imgUrl: 'assets/selection.png',
    },
    {
      featureList: ['Fresh', 'Modern', 'Trendy', 'Technical'],
      description:
        'Depending on your time, we give you the best look possible!',
      imgUrl: 'assets/training.png',
    },
    {
      featureList: ['Singing', 'Stage presence', 'Coordination', 'Depilation'],
      description: 'Need a helping hand? We got covered there too.',
      imgUrl: 'assets/goal.png',
    },
    {
      featureList: ['Nails', 'Skin', 'Feet', 'Depilation'],
      description: 'Need a helping hand? We got covered there too.',
      imgUrl: 'assets/goal.png',
    },
  ]
</script>

<SectionWrapper id="kurse">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center"></p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Kurse
      </h3>
    </div>
    {#each kurseFeatures as kurseFeature, index}
      <KurseCard {kurseFeature} {index}>
        {#if index === 0}
          Afrotanz als Sport <span class="text-red-500 font-medium"
            >& Bewegung
          </span>
        {:else if index === 1}
          Afro<span class="text-red-500 font-medium">Beats</span>
        {:else if index === 2}
          Gospel<span class="text-red-500 font-medium">chor</span>
        {:else}
          Stage <span class="text-red-500 font-medium">Company</span>
        {/if}
      </KurseCard>
    {/each}
  </div>
</SectionWrapper>
