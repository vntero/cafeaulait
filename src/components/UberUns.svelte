<script>
  import SectionWrapper from './SectionWrapper.svelte'
</script>

<SectionWrapper id="uberuns">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Unsere <span class="text-red-500">Geschichte</span>
      </h3>
    </div>

    <div>
      <div
        class="relative pt-16 pb-32 flex content-center items-center justify-center min-h-screen-75"
      >
        <img
          src="/assets/unseremission.png"
          alt="Uber uns"
          class="absolute top-0 w-full h-full rounded-lg shadow-md max-w-[1000px] mx-auto"
        />
      </div>

      <section class="pb-20 -mt-24">
        <div class="container mx-auto px-4">
          <div class="flex flex-wrap">
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
                  <h6 class="text-xl font-semibold">Love</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Café au Lait ist ein Verein für Afrotanz, Gesang &
                    Perkussion aus Zürich. Der Name ist Programm: So besteht
                    Café au Lait aus Kindern und Jugendlichen verschiedenster
                    Hautfarbe, Herkunft und Kultur.
                  </p>
                </div>
              </div>
            </div>

            <div class="w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-lightBlue-400"
                  >
                    <i class="fa-solid fa-child-reaching"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Movement</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Der Verein ist beim Sportamt Zürich als Jugendsportförderung
                    anerkannt. Café au Lait wurde im Herbst 2003 von der
                    gebürtigen Angolanerin Françoise Strassburg gegründet.
                  </p>
                </div>
              </div>
            </div>

            <div class="pt-6 w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="text-white p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-emerald-400"
                  >
                    <i class="fa-solid fa-bolt-lightning"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Passion</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Zusammen mit ihren Lehrerinnen und Lehrern fördert sie den
                    Tanz, die Rhythmik und den Gesang der jungen Künstlerinnen
                    und Künstlern bis hin zur Bühnenreife (siehe CAL Stage
                    Company). Dabei lernen die Kinder und Jugendlichen
                    spielerisch auch immer Respekt, gegenseitiges Verständnis
                    und Solidarität.
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
