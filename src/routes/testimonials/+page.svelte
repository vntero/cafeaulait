<script>
  import Footer from '../../components/Footer.svelte'
  import Header from '../../components/Header.svelte'
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  let reviewsList = [
    {
      name: 'Stadt Zürich',
      review:
        'Die Stadt Zürich hat am 24. November 2023 Françoise Strassburg, Gründerin und Präsidentin von Café au Lait, und ihre Weggefährt:innen mit dem Kulturpreis 2023 im Bereich Tanz & Theater gewürdigt. Wir sind überglücklich über diesen Preis und bedanken uns bei der Stadt Zürich.',
      features: ['Theater'],
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

<Header />
<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Stimmen <span class="text-red-500">über</span> uns
      </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each reviewsList as reviewItem, index}
          <div
            class={'flex flex-col gap-2 w-full max-w-[500px] mx-auto relative ' +
              (index % 2 === 1
                ? 'hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden'
                : ' ')}
          >
            <div class="flex relative">
              <div
                class={'absolute rounded-full bg-white aspect-square hidden md:grid place-items-center h-4 top-0 ' +
                  (index % 2 === 0
                    ? ' right-0 -mr-8 translate-x-1/2'
                    : ' left-0 -ml-8 -translate-x-1/2')}
              >
                <div class="rounded-full aspect-square bg-slate-950 h-2" />
              </div>
              <div class="flex items-center gap-2">
                <i class="fa-solid fa-user" />
                <h3 class="text-lg sm:text-xl md:text-2xl">
                  {reviewItem.name}
                </h3>
              </div>
            </div>
            <div class="h-[1.5px] bg-slate-950 w-1/4 mr-auto mb-4 mt-2"></div>
            <div
              class="flex items-center flex-wrap gap-2 text-xs sm:text-sm mb-4"
            >
              {#each reviewItem.features as keywork}
                <div
                  class="p-1 py-0.5 rounded-md border border-solid border-red-500 bg-red-50 text-red-500"
                >
                  <p>{keywork}</p>
                </div>
              {/each}
            </div>
            <p>{reviewItem.review}</p>
          </div>
        {/each}
      </div>
      <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
      <div class="flex flex-col gap-8">
        {#each reviewsList as reviewItem, index}
          <div
            class={'flex flex-col gap-2 w-full max-w-[500px] mx-auto relative ' +
              (index % 2 === 0
                ? 'hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden'
                : ' ')}
          >
            <div class="flex relative">
              <div
                class={'absolute rounded-full bg-white aspect-square hidden md:grid place-items-center h-4 top-0 ' +
                  (index % 2 === 0
                    ? ' right-0 -mr-8 translate-x-1/2'
                    : ' left-0 -ml-8 -translate-x-1/2')}
              >
                <div class="rounded-full aspect-square bg-slate-950 h-2" />
              </div>
              <div class="flex items-center gap-2">
                <i class="fa-solid fa-user" />
                <h3 class="text-lg sm:text-xl md:text-2xl">
                  {reviewItem.name}
                </h3>
              </div>
            </div>
            <div class="h-[1.5px] bg-slate-950 w-1/4 mr-auto mb-4 mt-2"></div>
            <div
              class="flex items-center flex-wrap gap-2 text-xs sm:text-sm mb-4"
            >
              {#each reviewItem.features as keywork}
                <div
                  class="p-1 py-0.5 rounded-md border border-solid border-red-500 bg-red-50 text-red-500"
                >
                  <p>{keywork}</p>
                </div>
              {/each}
            </div>
            <p>{reviewItem.review}</p>
          </div>
        {/each}
      </div>
    </div>
  </div>
</SectionWrapper>
<Footer />
