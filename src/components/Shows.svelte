<script>
  import Book from './Book.svelte'
  import SectionWrapper from './SectionWrapper.svelte'

  // Simplified showsList with exactly 2 items
  let showsList = [
    {
      name: 'Dein Event',
      review: `Brauchst du eine Showeinlage für deinen Anlass? Egal ob Firmenfeier, Hochzeit oder Sportanlass - unsere Performances reissen jedes Publikum mit und garantieren guten Laune. Kontaktiere uns, und sag uns, was du dir wünschst. Wir stellen dir ein massgeschneidertes Programm zusammen und freuen uns darauf, deinen Event zu einem unvergesslichen Highlight zu machen.`,
      features: ['Kulturpreis', '2023', 'Tanz & Theater'],
      buttonText: 'Mehr erfahren und buchen',
    },
    {
      name: 'Unsere Produktionen',
      review: `Wir erarbeiten regelmässig mit unseren Nachwuchstalenten und Künstler:innen neue Produktionen. Unsere neuste Produktion «R'Evolution» befasst sich mit struktureller Misogynie, derer nach wie vor alle weiblich gelesenen Menschen auf dieser Welt ausgesetzt sind.`,
      features: ['Authentizität', 'Kultur', 'Integration'],
      buttonText: 'Jetzt buchen und erleben',
    },
  ]
</script>

<SectionWrapper id="shows">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center pt-30"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Uns kannst du <span class="text-red-500">buchen</span>
      </h3>
    </div>
    <div class="container">
      <div class="items-center flex flex-wrap">
        <div class="w-full md:w-6/12">
          <h3 class="text-3xl font-semibold">Dein Event</h3>
          <p class="mt-4 text-lg leading-relaxed text-blueGray-500">
            Brauchst du eine Showeinlage für deinen Anlass? Egal ob Firmenfeier,
            Hochzeit oder Sportanlass - unsere Performances reissen jedes
            Publikum mit und garantieren guten Laune. Kontaktiere uns, und sag
            uns, was du dir wünschst. Wir stellen dir ein massgeschneidertes
            Programm zusammen und freuen uns darauf, deinen Event zu einem
            unvergesslichen Highlight zu machen.
          </p>
          <ul class="list-none mt-6">
            <li class="py-2">
              <div class="flex items-center">
                <div>
                  <span
                    class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-blueGray-500 bg-blueGray-50 mr-3"
                  >
                    <i class="fa-solid fa-bolt text-red-400"></i>
                  </span>
                </div>
                <div>
                  <h4 class="text-blueGray-500">Massgeschneidert</h4>
                </div>
              </div>
            </li>
            <li class="py-2">
              <div class="flex items-center">
                <div>
                  <span
                    class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-blueGray-500 bg-blueGray-50 mr-3"
                  >
                    <i class="fa-solid fa-bolt text-red-400"></i>
                  </span>
                </div>
                <div>
                  <h4 class="text-blueGray-500">Mitreissend</h4>
                </div>
              </div>
            </li>
            <li class="py-2">
              <div class="flex items-center">
                <div>
                  <span
                    class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-blueGray-500 bg-blueGray-50 mr-3"
                  >
                    <i class="fa-solid fa-bolt text-red-400"></i>
                  </span>
                </div>
                <div>
                  <h4 class="text-blueGray-500">Professionell</h4>
                </div>
              </div>
            </li>
          </ul>
          <br />
          <Book />
        </div>

        <div class="w-full md:w-6/12 px-4 pt-24 md:pt-0">
          <img
            alt="..."
            class="max-w-full rounded-lg shadow-xl"
            style="
            transform: scale(1) perspective(1040px) rotateY(-11deg)
              rotateX(2deg) rotate(2deg);
          "
            src="assets/shows.png"
          />
        </div>
      </div>
    </div>
  </div></SectionWrapper
>
