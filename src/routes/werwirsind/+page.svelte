<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'

  let team = [
    {
      name: 'Françoise Strassburg',
      role: 'Präsidentin & Initiantin',
      img: '/assets/pics/francoise.png',
    },
    {
      name: 'Deniz Tunbeceren',
      role: 'Koordination Events & Sponsoring',
      img: '/assets/pics/deniz.png',
    },
    {
      name: 'Sahara Kuhn',
      role: 'Tanzpädagogin & Admin',
      img: '/assets/pics/sahara.png',
    },
    {
      name: 'Flora Luvualu',
      role: 'Leitung Gesang',
      img: '/assets/pics/flora.png',
    },
    {
      name: 'Akim Princes',
      role: 'Tanzpädagoge traditioneller Tanz',
      img: '/assets/pics/akim.png',
    },
    {
      name: 'Altea Baumann',
      role: 'Gesangslehrerin',
      img: '/assets/pics/altea.png',
    },
    {
      name: 'Amélie Aragón ',
      role: 'Gesangslehrerin',
      img: '/assets/pics/amelie.png',
    },
    {
      name: 'Sékou Touré',
      role: 'Perkussionist',
      img: '/assets/pics/sekou.png',
    },
    {
      name: 'Urbain Guiguemdé',
      role: 'Theaterpädagoge',
      img: '/assets/pics/urbain.png',
    },
    {
      name: 'Yamoussa Sylla',
      role: 'Perkussionist',
      img: '/assets/pics/yamoussa.png',
    },
  ]

  let kids = [
    {
      name: 'Amaya',
      age: 8,
      origin: 'Côte d’Ivoire / Schweiz',
      img: '/assets/pics/amaya.png',
      quote:
        '"Ganz besonders gut gefällt mir das Trommeln. Manchmal fühlt sich Café au Lait wie meine Familie an."',
    },
    {
      name: 'Anisha',
      age: 14,
      origin: 'Angola / Südafrika',
      img: '/assets/pics/anisha.png',
      quote: null, // Quote missing
    },
    {
      name: 'Brimady',
      age: 11,
      origin: 'Kamerun / Schweiz',
      img: '/assets/pics/brimady.png',
      quote:
        '"Ich finde die traditionellen Tänze, das Singen und den Trommelunterricht toll und dass wir wie eine Familie sind."',
    },
    {
      name: 'Cherline',
      age: 11,
      origin: 'Haiti / Schweiz',
      img: '/assets/pics/cherline.png',
      quote:
        '"Mir gefällt, dass wir nicht nur tanzen, sondern auch singen, trommeln und zusammen essen und dass es jedes Jahr ein Lager gibt."',
    },
    {
      name: 'Debra',
      age: 15,
      origin: 'Nigeria / Schweiz',
      img: '/assets/pics/debra.png',
      quote:
        '"Mir gefällt es, dass wir alle wie eine grosse Familie sind und die Freude am Tanzen teilen. Ich geniesse die Zeit im Training immer sehr mit meinen Freunden."',
    },
    {
      name: 'Eléni',
      age: 12,
      origin: 'Griechenland / Jamaika / Schweiz',
      img: '/assets/pics/eleni.png',
      quote:
        '"Café au Lait ist meine zweite Familie. Es macht mir Spass, mich zur Musik zu bewegen und verschiedene Choreografien zu lernen."',
    },
    {
      name: 'Imani Melike',
      age: 14,
      origin: 'Schweiz / Togo / Türkei',
      img: '/assets/pics/imani.png',
      quote:
        '"Café au Lait ist wie eine grosse Familie und bietet mir die Möglichkeit, meine Leidenschaft, das Tanzen, auszuleben."',
    },
    {
      name: 'Imani',
      age: 14,
      origin: 'Belize / Brasilien / Schweiz',
      img: '/assets/pics/imanii.png',
      quote:
        '"Bei Café au Lait gefällt mir alles, vor allem aber dass wir zusammen tanzen können. Die Verbindung, die wir alle zueinander haben, ist speziell."',
    },
    {
      name: 'Juli',
      age: 11,
      origin: 'Schweiz / Tansania',
      img: '/assets/pics/juli.png',
      quote:
        '"Wir sind alle ein Team und kommen gut miteinander aus. Beim Tanzen fühle ich mich frei und es ist nicht schlimm, wenn man einen Fehler macht."',
    },
    {
      name: 'Kendra',
      age: 14,
      origin: 'Kamerun / Schweiz',
      img: '/assets/pics/kendra.png',
      quote: null, // Quote missing
    },
    {
      name: 'Lena',
      age: 15,
      origin: 'Kamerun',
      img: '/assets/pics/lena.png',
      quote: null, // Quote missing
    },
    {
      name: 'Lionelle',
      age: 13,
      origin: 'Côte d’Ivoire / Schweiz',
      img: '/assets/pics/lionelle.png',
      quote:
        '"Mir gefällt es bei Café au Lait, weil ich mich nicht verstecken muss. Wenn ich schlechte Laune habe, heitert mich das Tanzen immer auf."',
    },
    {
      name: 'Lishan',
      age: 13,
      origin: 'Äthiopien / Guadeloupe / Schweiz',
      img: '/assets/pics/lishan.png',
      quote:
        '"Es gefällt mir, dass wir immer neue Sachen und verschiedene Tanzstile lernen. Bei Café au Lait halten alle zusammen und wir stehen gerne auf der Bühne."',
    },
    {
      name: 'Luana',
      age: 14,
      origin: 'Kosovo / Nigeria / Schweiz',
      img: '/assets/pics/luana.png',
      quote:
        '"Bei Café au Lait vereint sich das Tanzen, Singen und Theater zu einer einzigartigen kreativen Gemeinschaft. Ich bin sehr froh und dankbar, Teil dieser tollen Gruppe zu sein."',
    },
    {
      name: 'Nerea',
      age: 9,
      origin: 'Côte d’Ivoire / Schweiz / Spanien',
      img: '/assets/pics/nerea.png',
      quote:
        '"Hier erlebe ich eine familiäre Atmosphäre. Ich fühle mich, so wie ich bin, vollkommen dazugehörig. Café au Lait ist eine Brücke zu meinen afrikanischen Wurzeln."',
    },
    {
      name: 'Salima',
      age: 13,
      origin: 'Gambia / Schweiz',
      img: '/assets/pics/salima.png',
      quote:
        '"Hier kann ich meine Kultur kennenlernen und bin in einer Tanzgruppe, in der alle zusammenhalten."',
    },
    {
      name: 'Solia',
      age: 13,
      origin: 'Italien / Nigeria / Schweiz',
      img: '/assets/pics/solia.png',
      quote:
        '"Café au Lait ist mehr als ein Hobby: Durch das gemeinsame Tanzen, Trommeln und Singen fühle ich mich verbunden mit meinen afrikanischen Wurzeln und mit den anderen TänzerInnen."',
    },
    {
      name: 'Sophie',
      age: 14,
      origin: 'Deutschland / Uganda',
      img: '/assets/pics/sophie.png',
      quote:
        '"Hier habe ich Freunde fürs Leben gefunden und ich fühle mich mehr zur afrikanischen Kultur verbunden."',
    },
    {
      name: 'Sydney',
      age: 14,
      origin: 'Côte d’Ivoire / Schweiz',
      img: '/assets/pics/sydney.png',
      quote:
        '"Café au Lait ist ein Ort, an dem du vieles auf einmal lernen kannst: Tanzen, Singen und Trommeln. Das jährliche Lager schweisst uns zusammen."',
    },
    {
      name: 'Tilala',
      age: 10,
      origin: 'Marokko / Schweiz / Senegal',
      img: '/assets/pics/tilala.png',
      quote:
        '"Hier kann ich so sein, wie ich bin und muss mich nicht verstellen. Ich fühle mich frei. Das macht mich sehr glücklich."',
    },
    {
      name: 'Yaiza',
      age: 14,
      origin: 'Côte d’Ivoire / Schweiz',
      img: '/assets/pics/yaiza.png',
      quote:
        '"Mir gefällt hier, dass ich mich so frei fühlen kann und immer neue Tanzarten lerne. Unser Zusammenhalt ist einzigartig."',
    },
  ]
</script>

<Header />
<!-- our values -->
<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Unser <span class="text-red-500">Verein</span>
      </h3>
    </div>

    <div>
      <div
        class="relative pt-16 pb-32 flex content-center items-center justify-center min-h-screen-75"
      >
        <img
          src="/assets/pics/unseremission.png"
          alt="Wer wir sind"
          class="absolute top-0 w-full h-full rounded-lg shadow-md max-w-[1000px] mx-auto"
        />
      </div>

      <section class="pb-20 -mt-24">
        <div class="container mx-auto px-4">
          <div class="flex flex-wrap">
            <!-- Swap first and second icon pls -->
            <div class="lg:pt-12 pt-6 w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="text-white p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-red-400"
                  >
                    <i class="fa-solid fa-heart"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Wer wir sind</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Wir sind ein Zürcher Verein für Afrotanz, Gesang, Schauspiel
                    & Perkussion. Unser Angebot ist allen Kindern zugänglich
                    unabhängig von ihrer Hautfarbe, Herkunft und Konfession.
                    Unsere Arbeit ist beim Sportamt Zürich als
                    Jugendsportförderung anerkannt.
                  </p>
                </div>
              </div>
            </div>

            <!-- Unser Ziel -->
            <div class="w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-lightBlue-400"
                  >
                    <i class="fa-solid fa-arrows-to-circle"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Unser Ziel</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Mit unserem Angebot wollen wir die Diversität der Schweizer
                    Gesellschaft sichtbar machen und einen Beitrag zu mehr
                    Toleranz und Dialog leisten. Unsere Produktionen behandeln
                    deshalb gesellschaftskritische Themen und im Unterricht
                    lernen die Schüler:innen spielerisch Respekt, gegenseitiges
                    Verständnis und Solidarität.
                  </p>
                </div>
              </div>
            </div>

            <!-- Idea: Icon should be roots -->
            <div class="pt-6 w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="text-white p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-emerald-400"
                  >
                    <i class="fa-solid fa-seedling"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Woher wir kommen</h6>

                  <p class="mt-2 mb-4 text-blueGray-500">
                    Café au Lait wurde 2003 von der gebürtigen Angolanerin,
                    Françoise Strassburg, gegründet. Seither haben unsere
                    Pädagog:innen bereits mehrere hundert Kinder von ihren
                    ersten Tanzschritten bis hin zur Bühnenreife begleitet.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</SectionWrapper>

<!-- our team -->
<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Unser <span class="text-red-500">Team</span>
      </h3>
    </div>
    <div
      class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10 md:gap-14 w-full"
    >
      {#each team as member}
        <div
          class="flex flex-col gap-2 text-left max-w-[400px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <div class="flex items-center gap-4">
            <img
              src={member.img}
              alt={member.name}
              class="w-20 h-20 rounded-full object-cover shadow-md"
            />
            <h4 class="text-lg sm:text-xl md:text-2xl pt-2 text-red-500">
              {member.name}
            </h4>
          </div>
          <p class="pl-2">{member.role}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>

<!-- our kids -->
<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Unser <span class="text-red-500">Nachwuchs</span>
      </h3>
    </div>
    <div
      class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10 md:gap-14 w-full"
    >
      {#each kids as kid}
        <div
          class="group flex flex-col gap-2 text-left max-w-[400px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <div class="relative flex items-center gap-4">
            <img
              src={kid.img}
              alt={kid.name}
              class="w-20 h-20 rounded-full object-cover shadow-md"
            />
            <h4 class="text-lg sm:text-xl md:text-2xl pt-2 text-red-500">
              {kid.name}
            </h4>
            <!-- Chat bubble appears on hover if quote is present -->
            {#if kid.quote}
              <div
                class="chat chat-start absolute left-24 bottom-12 hidden group-hover:block"
              >
                <div class="chat-bubble bg-red-200 text-black">
                  <i>{kid.quote}</i>
                </div>
              </div>
            {/if}
          </div>
          <p class="pl-2">{kid.age}, {kid.origin}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>

<Footer />
