<script>
  import SectionWrapper from './SectionWrapper.svelte'
  import Register from './Register.svelte'
  import Kursplan from './Kursplan.svelte'

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
      imgUrls: ['assets/pics/tanzkurse.png'],
    },
    {
      featureList: ['Mehrstimmiger Gesang', 'Stimmbildung', 'Gehörbildung'],
      description:
        'Mit dem Chor treten wir an unterschiedlichen Anlässen auf und erarbeiten Stücke für unsere Eigenproduktionen.',
      imgUrls: [
        'assets/pics/chor.png',
        // 'assets/pics/gospel2.png',
      ],
    },
    {
      featureList: ['Bühnenpräsenz', 'Theater', 'Tanz', 'Perkussion'],
      description:
        'In der CAL Stage Company fördern wir deine Bühnenreife. Du erarbeitest und probst neue Produktionen mit der ganzen Companie und kannst zeigen, was du drauf hast.',
      imgUrls: [
        'assets/pics/stage.png',
        // 'assets/pics/stage2.png',
        // 'assets/pics/stage3.png',
      ],
    },
    {
      featureList: ['Afrobeats', 'Attitude', 'Technik'],
      description:
        'Bist du mindestens 12 Jahre alt und hast was auf dem Kasten? Dann richtet sich dieser Kurs an dich. Junge Tanzlehrer:innen und Erstplatzierte an der "World of Dance Switzerland 2023" zeigen dir freshe Moves für Fortgeschrittene und vermitteln dir Attitude für die Bühne.',
      imgUrls: [
        'assets/pics/kurse2.png',
        // 'assets/pics/afrobeats2.png',
      ],
    },
  ]
</script>

<SectionWrapper id="kurse">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14 pt-20"
  >
    <!-- Section title -->
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center"></p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Kurse
      </h3>
    </div>

    {#each kurseFeatures as kurseFeature, index}
      <div
        class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-14 lg:gap-20 relative text-base"
      >
        <!-- Courses and descriptions -->
        <div
          class={'flex flex-col gap-8 md:gap-10 pt-8 sm:pt-10' +
            (index % 2 === 1 ? ' md:order-2' : ' ')}
        >
          <h4
            class="text-2xl sm:text-3xl md:text-4xl font-medium relative pr-10 after:absolute after:top-full after:left-0 after:w-1/5 after:h-1.5 after:mt-1 after:bg-slate-900"
          >
            {#if index === 0}
              Tanz<span class="text-red-500 font-medium">kurse </span>
            {:else if index === 1}
              CAL <span class="text-red-500 font-medium">Chor</span>
            {:else if index === 2}
              Stage <span class="text-red-500 font-medium">Company</span>
            {:else}
              Afrobeats <span class="text-red-500 font-medium">Masterclass</span
              >
            {/if}
          </h4>
          <p>{kurseFeature.description}</p>
          <div class="flex flex-col gap-3 mt-0">
            {#each kurseFeature.featureList as listItem}
              <div class="flex gap-2 items-center">
                <div
                  class="grid place-items-center px-1.5 text-xs sm:text-sm aspect-square rounded-full border-[1.5px] bg-white border-solid border-red-300"
                >
                  <i class="fa-solid fa-bolt text-red-400"></i>
                </div>
                <p>{listItem}</p>
              </div>
            {/each}
          </div>

          <!-- Buttons to open modals -->
          <div class="flex items-center gap-4">
            <Register />
            <Kursplan />
          </div>
        </div>
        <!-- CAROUSEL -->
        <div class="carousel rounded-box space-x-2 h-96 max-w-[1000px] mt-14">
          {#each kurseFeature.imgUrls as imgUrl}
            <div class="carousel-item flex-shrink-0 w-full snap-start">
              <img
                src={imgUrl}
                alt="kurse"
                class="object-cover w-full h-full rounded-lg"
              />
            </div>
          {/each}
        </div>
      </div>
    {/each}
  </div>
</SectionWrapper>
