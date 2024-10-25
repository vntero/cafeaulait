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
    <!-- <div
      class="diff aspect-[16/2] rounded-lg max-w-[1000px] mx-auto w-full text-center"
    >
      <div class="diff-item-1">
        <div
          class="bg-gray-100 text-xl lg:text-5xl md:text-3xl sm:text-2xl text-center grid place-content-center font-black font-semibold"
        >
          vom Hauch eines neuen Lebens
        </div>
      </div>
      <div class="diff-item-2">
        <div
          class="bg-black grid place-content-center text-5xl sm:text-6xl md:text-7xl text-white font-semibold"
        >
          Le Souffle
        </div>
      </div>
      <div class="diff-resizer"></div>
    </div> -->
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

    <!-- CAROUSEL -->
    <div class="carousel rounded-box space-x-2 h-64 max-w-[1000px]">
      <div class="carousel-item">
        <img src="assets/ls1.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls2.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls3.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls4.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls5.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls6.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls7.png" alt="le souffle" />
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
          >„Le Souffle – vom Hauch eines neuen Lebens“</span
        >. Sie geht eine brand-aktuelle Thematik an, die
        <span class="text-red-500">polarisiert</span>. Mit diesem Stück wagt
        sich CAL an <span class="text-red-500">sensitive Themen</span>, die den
        Nerv der Gesellschaft treffen und spricht dabei über Migration,
        Hoffnung, Fremdenhass, Integration, Mischlingskinder und Liebe. Das
        Stück handelt vom Aufbruch in eine neue, hoffentlich bessere Welt, den
        zahlreiche Migrantinnen und Migranten wagen.
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
    </div>

    <!-- PAST SHOWS
    <div
      class="max-w-[1000px] mx-auto w-full text-center bg-[#FFF1DB] p-6 rounded-lg shadow-lg"
    >
      <h3 class="text-4xl font-semibold mb-6">Frühere Shows:</h3>
      <ul class="list-disc list-inside text-left mx-auto max-w-lg">
        {#each shows as show}
          <li class="mb-4">
            <span class="font-semibold">{show.date}</span> @ {show.location}
          </li>
        {/each}
      </ul>
    </div> -->
  </div>
</SectionWrapper>
<Footer />
