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
        Unser <span class="text-red-500">Verein</span>
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
            <!-- Diversität -->
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
                  <h6 class="text-xl font-semibold">Diversität</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Café au Lait ist ein Verein für Afrotanz, Gesang &
                    Perkussion aus Zürich. Der Name ist Programm: Café au Lait
                    besteht aus Kindern und Jugendlichen unterschiedlicher
                    Hautfarben, Herkunft und Kultur.
                  </p>
                </div>
              </div>
            </div>

            <!-- Ursprung -->
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
                  <h6 class="text-xl font-semibold">Ursprung</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Der Verein wurde 2003 von der gebürtigen Angolanerin
                    Françoise Strassburg gegründet und ist beim Sportamt Zürich
                    als Jugendsportförderung anerkannt.
                  </p>
                </div>
              </div>
            </div>

            <!-- Mission -->
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
                  <h6 class="text-xl font-semibold">Mission</h6>
                  <p class="mt-2 mb-4 text-blueGray-500">
                    Café au Lait fördert die jungen Künstlerinnen und Künstlern
                    in Tanz, Rhythmik, Schauspiel und Gesang bis hin zur
                    Bühnenreife (<a
                      href="/"
                      class="text-red-500 hover:text-blue-600"
                    >
                      siehe Stage Company</a
                    >). Dabei lernen die Kinder und Jugendlichen spielerisch
                    auch Respekt, gegenseitiges Verständnis und Solidarität.
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
