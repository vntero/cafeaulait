<script>
  import SectionWrapper from './SectionWrapper.svelte'
  import Header from './Header.svelte'
  import Book from './Book.svelte'
  import Register from './Register.svelte'

  let events = [
    {
      date: '15.06.2025',
      title: `Premiere "R'Evolution"`,
      location: 'Volkshaus, Zürich - Save the date!',
    },
    {
      date: '26.09.2025',
      title: `R'Evolution`,
      location: 'Kurhotel, Baden  - Infos folgen',
    },
  ]
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-10 flex-1 items-center mt-16">
    <h2
      class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold"
    >
      Café au Lait
    </h2>
    <p
      class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
    >
      <span class="italic"
        >Die Afrotanzgruppe aus Zürich für Kinder & Jugendliche</span
      >
    </p>
    <a
      href="https://www.stadt-zuerich.ch/de/aktuell/medienmitteilungen/2023/10/231024a2.html"
      target="_blank"
      class="flex items-center transition-transform duration-300 hover:scale-110"
    >
      <img
        src="/assets/pics/zuri.png"
        alt="zuri"
        class="w-10 sm:w-10 md:w-10 lg:w-10"
      />
      <p>Kulturpreis Kanton Zürich “Tanz & Theater”</p>
    </a>

    <!-- Main image -->
    <img
      src="/assets/pics/afrosummerjam.png"
      alt="Kinder"
      class="w-full max-w-[1000px] mx-auto rounded-lg shadow-md"
    />

    <div class="flex items-center gap-4">
      <Book />
      <Register />
    </div>

    <!-- Upcoming Events Section -->
    <div
      class="max-w-[1000px] mx-auto w-full text-center bg-[#FFF1DB] p-6 rounded-lg shadow-lg"
    >
      <h3 class="text-4xl font-semibold mb-6">Upcoming Events</h3>
      <ul class="list-disc list-inside text-left mx-auto max-w-[600px]">
        {#each events as event}
          <li class="mb-4">
            <span class="font-semibold">{event.date}</span>: {event.title}
            <span class="italic">@ {event.location}</span>
          </li>
        {/each}
      </ul>
    </div>
  </div>
</SectionWrapper>
