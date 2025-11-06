<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'

  let team = [
    {
      name: 'Françoise Strassburg',
      role: 'Gründerin',
      img: '/assets/pics/francoise.png',
    },
    {
      name: 'Amélie Aragón Kpenou',
      role: 'Co-Leiterin & Gesangsleiterin',
      img: '/assets/pics/amelie.png',
    },
    {
      name: 'Sahara Kuhn',
      role: 'Co-Leiterin & Tanzpädagogin Afrobeats',
      img: '/assets/pics/sahara.png',
    },
    {
      name: 'Deniz Tunbeceren',
      role: 'Koordinatorin Events & Sponsoring',
      img: '/assets/pics/deniz.png',
    },
    {
      name: 'Akim Princes',
      role: 'Tanzpädagoge traditioneller Tanz',
      img: '/assets/pics/akim.png',
    },
    {
      name: 'Flora Luvualu',
      role: 'Gesangspädagogin',
      img: '/assets/pics/flora.png',
    },
    {
      name: 'Urbain Guiguemdé',
      role: 'Theaterpädagoge',
      img: '/assets/pics/urbain.png',
    },
    {
      name: 'Sékou Touré',
      role: 'Perkussionist',
      img: '/assets/pics/sekou.png',
    },
    {
      name: 'Yamoussa Sylla',
      role: 'Perkussionist',
      img: '/assets/pics/yamoussa.png',
    },
  ]
</script>

<Header />
<!-- our values -->
<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-50 flex-1 items-center justify-center"
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
          src="/assets/pics/unser-verein.png"
          alt="Wer wir sind"
          class="absolute top-0 w-full rounded-lg shadow-md max-w-[1000px] mx-auto"
        />
      </div>

      <section class="pb-20 -mt-24">
        <div class="container mx-auto px-4">
          <div class="flex flex-wrap">
            <!-- Wer wir sind -->
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
                    & Perkussion. Unser Angebot ist allen Kindern zugänglich,
                    unabhängig von ihrer Hautfarbe, Herkunft und Konfession.
                    Unsere Arbeit ist beim Sportamt Zürich als
                    Jugendsportförderung anerkannt und wurde 2023 von der Stadt
                    Zürich mit dem Kulturpreis im Bereich Tanz & Theater
                    gewürdigt.
                  </p>
                </div>
              </div>
            </div>

            <!-- Unser Ziel -->
            <div class="w-full md:w-4/12 px-4 py-20 text-center">
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

            <!-- Woher wir kommen -->
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

<Footer />
