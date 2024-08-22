<script>
  import SectionWrapper from './SectionWrapper.svelte'

  // Simplified showsList with exactly 2 items
  let showsList = [
    {
      name: 'Dein Event',
      review: `Egal, ob Firmenfeier, Hochzeit oder eine coole Party – unsere Shows garantieren jede Menge Spass und gute Laune. Lass dich von unseren Performances und der Energie mitreißen! Kontaktiere uns, um mehr über unser Angebot zu erfahren. Wir freuen uns darauf, deinen Event zu einem unvergesslichen Highlight zu machen.`,
      features: ['Kulturpreis', '2023', 'Tanz & Theater'],
      buttonText: 'Mehr erfahren und buchen',
    },
    {
      name: 'Unsere Produktionen',
      review: `Unsere Hauptproduktion bringt die faszinierenden Geschichten afrikanischer Einwanderer in Europa auf die Bühne. Mit lebhaften Tänzen und mitreißender Musik feiern wir die Stärke und Kreativität dieser Gemeinschaft. Erleben Sie, wie kulturelle Vielfalt und persönliche Geschichten zu einer beeindruckenden und inspirierenden Performance verschmelzen.`,
      features: ['Authentizität', 'Kultur', 'Integration'],
      buttonText: 'Jetzt buchen und erleben',
    },
  ]
</script>

<SectionWrapper id="shows">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Uns kann man <span class="text-red-500">buchen</span>
      </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      {#each showsList as showsItem, index}
        <div class="flex flex-col gap-2 w-full max-w-[500px] mx-auto relative">
          <div class="flex relative">
            <div class="flex items-center gap-2">
              <h3 class="text-lg sm:text-xl md:text-2xl">
                {showsItem.name}
              </h3>
            </div>
          </div>
          <div class="h-[1.5px] bg-slate-950 w-1/4 mr-auto mb-4 mt-2"></div>
          <div
            class="flex items-center flex-wrap gap-2 text-xs sm:text-sm mb-4"
          >
            <!-- {#each showsItem.features as keyword}
              <div
                class="p-1 py-0.5 rounded-md border border-solid border-red-500 bg-red-50 text-red-500"
              >
                <p>{keyword}</p>
              </div>
            {/each} -->
          </div>
          <p>{showsItem.review}</p>
          <div class="flex items-center gap-4">
            <button class={index === 1 ? 'specialBtn' : 'specialBtnDark'}>
              <p class="text-base sm:text-lg md:text-xl">
                {showsItem.buttonText}
              </p>
            </button>
          </div>
        </div>
        <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
      {/each}
    </div>
  </div>
</SectionWrapper>
