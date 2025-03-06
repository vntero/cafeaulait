<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'

  let shows = [
    {
      date: '27.11.2021',
      location: 'Schwertsaal, Wald ZH',
      info: 'https://www.agkultur.ch/agenda/cafe-au-lait-le-souffle-vom-hauch-eines-neuen-lebens/',
    },
    {
      date: '01.12.2018',
      location: 'Rote Fabrik, Zürich',
      info: 'https://rotefabrik.ch/#/events/1959?utm_medium=display&utm_source=kulturzueri.ch&utm_campaign=kulturzueri',
    },
    {
      date: '16.06.2018',
      location: 'Volkhaus, Zürich',
      info: 'https://rotefabrik.ch/#/events/1959?utm_medium=display&utm_source=kulturzueri.ch&utm_campaign=kulturzueri',
    },
    {
      date: '13.05.2018',
      location: 'Wolfhalden, Appenzell Ausserrhoden',
      info: 'https://www.tagblatt.ch/ostschweiz/rheintal/poetry-slam-an-der-songwriter-nacht-ld.524936',
    },
  ]
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-10 flex-1 items-center mt-16">
    <!-- LE SOUFFLE - DIFF SLIDER TITLE -->
    <!-- Slider code is commented out, if you wish to keep, you can implement your own or use a simple tailwind transition. -->

    <div class="flex flex-col gap-2 mt-20">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center"></p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Le <span class="text-red-500">Souffle</span>
      </h3>
    </div>

    <!-- SHORT DESCRIPTION AND PRODUCER -->
    <div class="flex flex-col gap-2">
      <p
        class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
      >
        <span class="italic">"Le Souffle" - vom Hauch eines neuen Lebens</span>
      </p>
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Eine Produktion von <span class="text-red-500"
          >Françoise Strassburg</span
        >
      </p>
    </div>

    <!-- CAROUSEL (Replaced DaisyUI Carousel with custom flex/grid layout) -->
    <div
      class="flex overflow-x-auto space-x-4 w-[500px] sm:w-[750px] md:sm:w-[900px] lg:sm:w-[1000px]"
    >
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls1.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls2.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls3.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls4.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls5.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls6.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
      <div class="flex-none w-52 h-72 rounded-lg bg-gray-100 overflow-hidden">
        <img
          src="assets/pics/ls7.png"
          alt="le souffle"
          class="object-cover w-full h-full"
        />
      </div>
    </div>

    <!-- PRODUCTION DESCRIPTION -->
    <div class="flex flex-col gap-2">
      <p class="text-base sm:text-lg md:text-xl text-justify max-w-[1000px]">
        <span class="text-red-500">Provokativ</span>,
        <span class="text-red-500">berührend</span>,
        <span class="text-red-500">wortlos</span>,
        <span class="text-red-500">witzig</span>. Das ist unsere jüngste
        Produktion namens
        <span class="text-red-500"
          >„Le Souffle – vom Hauch eines neuen Lebens”</span
        >. Sie geht eine brandaktuelle Thematik an, die
        <span class="text-red-500">polarisiert</span>. Mit diesem Stück wagt
        sich CAL an
        <span class="text-red-500">sensitive Themen</span>, die den Nerv der
        Gesellschaft treffen und spricht dabei über Migration, Hoffnung,
        Fremdenhass, Integration, Mischlingskinder und Liebe. Das Stück handelt
        vom Aufbruch in eine neue, hoffentlich bessere Welt, den zahlreiche
        Migrantinnen und Migranten wagen.
      </p>
      <p class="text-base sm:text-lg md:text-xl text-justify max-w-[1000px]">
        Die anfängliche Freude, aber auch die Gefahren und Trauer auf diesem Weg
        werden von CALs Nachwuchstalenten sowie von professionellen Tänzern
        Afrikas mit <span class="text-red-500">farbenfrohen Kostümen</span>,
        <span class="text-red-500">atemberaubenden Tänzen</span>, pulsierenden
        Trommeln und betörenden Gesängen dargestellt. Ein Muss für Liebhaber des
        traditionellen und zeitgenössischen afrikanischen Tanzes und alle, die
        ihren Horizont erweitern wollen.
      </p>
      <span class="text-red-500">Provokativ</span>,
      <span class="text-red-500">herzzerreissend</span>,
      <span class="text-red-500">wortlos</span> und manchmal
      <span class="text-red-500">lustig</span>. Das ist die Produktion „Le
      Souffle – vom Hauch eines neuen Lebens“. Mit diesem Stück wagen wir uns an
      Themen, die berühren und polarisieren: Migration, Hoffnung,
      Fremdenfeindlichkeit, Integration, Identität und Liebe. Es erzählt von
      Menschen, die den mutigen Schritt in eine neue, hoffnungsvollere Welt
      wagen. Die anfängliche Freude, aber auch die Herausforderungen und Trauer
      auf diesem Weg werden von Café au Laits Nachwuchstalenten sowie
      professionellen Künstlerinnen und Künstlern eindrucksvoll zum Leben
      erweckt – mit farbenfrohen Kostümen, atemberaubenden Choreografien,
      pulsierenden Trommeln und mitreissendem Gesang. Ein Muss für
      Liebhaberinnen und Liebhaber des traditionellen und zeitgenössischen
      afrikanischen Tanzes und für alle, die ihren Horizont erweitern möchten.
    </div>
  </div>
</SectionWrapper>
<Footer />
