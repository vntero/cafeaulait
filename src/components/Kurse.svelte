<script>
  import { onMount } from 'svelte'
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
      imgUrl: 'assets/pics/kurse1.png',
    },
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

  let currentSlide = 0

  function nextSlide() {
    currentSlide = (currentSlide + 1) % kurseFeatures.length
  }

  function prevSlide() {
    currentSlide =
      (currentSlide - 1 + kurseFeatures.length) % kurseFeatures.length
  }

  onMount(() => {
    const interval = setInterval(nextSlide, 5000) // Auto-change slide every 5 seconds
    return () => clearInterval(interval) // Clean up the interval on component destroy
  })
</script>

<SectionWrapper id="kurse">
  <div class="flex flex-col gap-10 items-center pb-10 pt-20">
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base text-center"></p>
      <h3 class="text-4xl font-semibold text-center">Kurse</h3>
    </div>

    <!-- Slide Display -->
    {#each kurseFeatures as kurseFeature, index}
      {#if index === currentSlide}
        <div class="grid grid-cols-1 md:grid-cols-2 gap-14 text-base">
          <!-- Text Content Always on the Left -->
          <div class="flex flex-col gap-8 pt-8">
            <h4 class="text-2xl font-medium relative pr-10">
              {#if index === 0}
                Tanz<span class="text-red-500">kurse</span>
              {:else if index === 1}
                Afrobeats <span class="text-red-500">Masterclass</span>
              {:else if index === 2}
                CAL <span class="text-red-500">Chor</span>
              {:else}
                Stage <span class="text-red-500">Company</span>
              {/if}
            </h4>
            <p>{kurseFeature.description}</p>
            <div class="flex flex-col gap-3">
              {#each kurseFeature.featureList as listItem}
                <div class="flex gap-2 items-center">
                  <div
                    class="px-1.5 text-xs rounded-full border bg-white border-red-300"
                  >
                    <i class="fa-solid fa-bolt text-red-400"></i>
                  </div>
                  <p>{listItem}</p>
                </div>
              {/each}
            </div>
            <div class="flex items-center gap-4">
              <Register />
              <Kursplan />
            </div>
          </div>

          <!-- Image Content Always on the Right -->
          <div class="flex dropShadow overflow-hidden rounded-b-lg">
            <div
              class="rounded-t-xl h-8 bg-white opacity-60 px-3 flex items-center gap-2"
            >
              {#each [1, 2, 3] as i}
                <div class="rounded-full w-3 bg-red-500" />
              {/each}
            </div>
            <img
              src={kurseFeature.imgUrl}
              alt="kurse-img"
              class="flex flex-col bg-white sm:w-full"
            />
          </div>
        </div>
      {/if}
    {/each}

    <!-- Navigation Controls -->
    <div class="flex items-center gap-4 mt-4">
      <!-- Previous Button -->
      <button on:click={prevSlide}>
        <i class="fa-solid fa-circle-arrow-left text-red-400 text-3xl"></i>
      </button>

      <!-- Slide Indicators -->
      <div class="flex gap-2">
        {#each kurseFeatures as _, dotIndex}
          <div
            class="w-3 h-3 rounded-full transition-colors"
            class:bg-red-400={dotIndex === currentSlide}
            class:bg-red-300={dotIndex !== currentSlide}
          ></div>
        {/each}
      </div>

      <!-- Next Button -->
      <button on:click={nextSlide}>
        <i class="fa-solid fa-circle-arrow-right text-red-400 text-3xl"></i>
      </button>
    </div>
  </div>
</SectionWrapper>
