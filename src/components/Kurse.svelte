<script>
  import KurseCard from './KurseCard.svelte'
  import SectionWrapper from './SectionWrapper.svelte'
  let kurseFeatures = [
    {
      featureList: [
        'Traditional',
        'Afrobeats',
        'Contemporary',
        'Percussion Dance',
      ],
      description:
        'Für alle Niveaus ab 6 Jahren. Lerne in unseren Kursen unterschiedliche Tanzstile aus dem afrikanischen Kontinent.',
      imgUrl: 'assets/pics/kurse1.png',
    },

    // (Afrobeats Masterclass)
    {
      featureList: ['Afrobeats', 'Attitude', 'Technik'],
      description:
        'Bist du mindestens 12 Jahre alt und hast es richtig drauf? Dann richtet sich dieser Kurs an dich. Junge Tanzlehrer:innen und Erstplatzierte an der "World of Dance Switzerland 2023" zeigen dir freshe Moves für Fortgeschrittene und vermitteln dir Attitude für die Bühne.',
      imgUrl: 'assets/pics/kurse2.png',
    },
    {
      featureList: [
        'Mehrstimmiger Gesang',
        'Stimmbildung',
        'Musikalisches Hören & Harmonie',
      ],
      description:
        'Mit dem Chor treten wir an unterschiedlichen Anlässen auf und erarbeiten Stücke für Eigenproduktionen.',
      imgUrl: 'assets/pics/kurse3.png',
    },
    {
      featureList: ['Bühnenpräsenz', 'Theater', 'Tanz', 'Perkussion'],
      description:
        'In der CAL Stage Company fördern wir deine Bühnenreife. Du erarbeitest und probst neue Produktionen mit der ganzen Companie und kannst zeigen, was du drauf hast.',
      imgUrl: 'assets/pics/kurse4.png',
    },
  ]
</script>

<SectionWrapper id="kurse">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14 pt-20"
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
          Tanz<span class="text-red-500 font-medium">kurse </span>
        {:else if index === 1}
          Afrobeats <span class="text-red-500 font-medium">Masterclass</span>
        {:else if index === 2}
          CAL <span class="text-red-500 font-medium">Chor</span>
        {:else}
          Stage <span class="text-red-500 font-medium">Company</span>
        {/if}
      </KurseCard>
    {/each}
  </div>
</SectionWrapper>
