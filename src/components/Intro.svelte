<script>
  import SectionWrapper from './SectionWrapper.svelte'
  import Header from './Header.svelte'
  import Book from './Book.svelte'
  import Register from './Register.svelte'

  let events = [
    {
      date: '17.11.2024',
      title: `Premiere "R'Evolution" - Save the date!`,
      location: 'Volkshaus, Zürich',
    },
  ]

  let reviewsList = [
    {
      name: 'Stadt Zürich',
      review:
        'Die Stadt Zürich hat am 24. November 2023 Françoise Strassburg, Gründerin und Präsidentin von Café au Lait, und ihre Weggefährt:innen mit dem Kulturpreis 2023 im Bereich Tanz & Theater gewürdigt. Wir sind überglücklich über diesen Preis und bedanken uns bei der Stadt Zürich.',
      features: ['Kulturpreis 2023', 'Bereich Tanz', 'Theater'],
      link: 'https://www.stadt-zuerich.ch/prd/de/index/ueber_das_departement/medien/medienmitteilungen/2023/oktober/231024a.html',
    },
    {
      name: 'Moni Henzler - Kinderfest Knonau für Afrika',
      review:
        'Café au Lait, ihr habt unsere Bühne gerockt. Es war mir eine grosse Ehre und noch grössere Freude, euch für unseren Anlass zu gewinnen. Die Lebensfreude, die ihr versprüht, hat mein Herz erwärmt.',
      features: [],
    },
    {
      name: 'Max Pflüger - Ostschweiz am Sonntag',
      review:
        'Erzählt bildhaft von Erlebnissen afrikanischer Migranten. Ohne Worte und dennoch ausdrucksstark.',
      features: [],
    },
    {
      name: 'Zoe Venakis / Julia Bendlin - SRF',
      review:
        'In der grossen Turnhalle des Zürcher Gemeinschaftszentrums Riesbach klingen laute Trommeln. Man versteht kaum sein eigenes Wort. Der Boden vibriert und die Haare der Mädchen schleudern durch die Luft. Es ist Probe bei Café au Lait – einem Verein zur Pflege panafrikanischer Volkstänze. Schweisstreibend ist der Tanz. Doch nur um Fitness geht es hier nicht.',
      features: ['Identität', 'Integration', 'Volkstanz'],
      link: 'https://www.srf.ch/kultur/gesellschaft-religion/volkstanz-im-aufwind-herz-und-fuesse-tanzen-im-takt',
    },
    {
      name: 'Zeno van Essel - STAGEPLANET',
      review:
        'Ihre Wurzeln sind in Kamerun, Kongo, Togo, Kamerun, Jamaica und anderen Orten der Karibik, Afrikas und Asiens. Ihre Wurzeln sind aber auch hier in der Schweiz, dem Land, wo sie aufwachsen und dessen Dialekt sie sprechen. Zusammen bilden diese Kinder und Jugendlichen verschiedenster Hautfarbe, Herkunft und Kultur die Tanztruppe Café au Lait, die der Schweizer Kultur ein wichtiges Stück neuer, kraftvoller Authentizität hinzufügt.',
      features: ['Leidenschaftlich', 'Kraftvoll', 'Schön'],
      link: 'https://stageplanet.ch/2018/05/cafe-au-lait/',
    },
    {
      name: 'Klaus Merz - Schriftsteller',
      review:
        'Die Produktion “Le Souffle” ist nicht nur herzzerreissend schön, sondern auch künstlerisch klug durchdacht. Flankiert von achtsamen Trommeln und Tänzern und ebenso virtuosem Gesang tanzen und atmen unsere Kinder und Menschenskinder – tragend und getragen – in der wogenden Schar.',
      features: [],
    },
    {
      name: 'Josette Stehli - eine Zuschauerin',
      review:
        "Le Souffle est une histoire humaine qui remue l'âme au plus profond. Le coeur explose en émotions qui ne peuvent se cacher. Un cri, un seul, nous transperce... qui porte en lui tous les mots de toutes les langues de notre terre. Le mouvement, le rythme, le silence sont l'expression de cette force courageuse qui porte l'homme sur le sentier universel vers l'accueil de toute vie. Merci Café au Lait.",
      features: [],
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
      <ul class="list-disc list-inside text-left mx-auto max-w-lg">
        {#each events as event}
          <li class="mb-4">
            <span class="font-semibold">{event.date}</span>: {event.title}
            <br />
            <span class="italic">{event.location}</span>
          </li>
        {/each}
      </ul>
    </div>
  </div>
</SectionWrapper>
