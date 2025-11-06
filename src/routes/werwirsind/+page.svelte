<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
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

<Footer />
