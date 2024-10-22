<script>
  import KurseCard from './KurseCard.svelte'
  import SectionWrapper from './SectionWrapper.svelte'
  let kurseFeatures = [
    {
      featureList: [
        'Ab 6 Jahren',
        'Koordination',
        'Rhythhmus',
        'Live-Perkussion',
      ],
      description:
        'Lerne traditionelle Tänze aus verschiedenen afrikanischen Ländern - egal ob du Anfänger:in oder auf fortgeschrittenem Niveau bist.',
      imgUrl: 'assets/kurse1.png',
    },
    {
      featureList: ['Frisch', 'Modern', 'Trendig', 'Technisch'],
      description:
        'Junge Tänzerinnen und Tänzer vermitteln energiereiche Schritte und freshe Vibes.',
      imgUrl: 'assets/kurse2.png',
    },
    {
      featureList: ['Singen', 'Bühnenpräsenz', 'Koordination', 'Stimme'],
      description:
        'Die «CAL Stage Company» ist eine bühnenorientierte Tanzgruppe. Sie hat zum Ziel, die künstlerische Ausbildung im Bereich des traditionellen und zeitgenössischen afrikanischen Tanzes, der Perkussion und des Gesangs zu fördern.',
      imgUrl: 'assets/kurse3.png',
    },
    {
      featureList: ['Bühnenpräsenz', 'Wirkung', 'Koordination', 'Stärke'],
      description:
        'Der «CAL Chor» ist ein bühnenorientierter Chor, der an den unterschiedlichsten Anlässen auftritt und an den Produktionen der «CAL Stage Company» mitarbeitet.',
      imgUrl: 'assets/kurse4.png',
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
          Traditional <span class="text-red-500 font-medium">Dance </span>
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
