<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'

  let team = [
    {
      name: 'Françoise Strassburg',
      role: 'Präsidentin & Initiantin',
      img: '/assets/francoise.png',
    },
    {
      name: 'Deniz Tunbeceren',
      role: 'Admin',
      img: '/assets/deniz.png',
    },
    {
      name: 'Sophia Banghal',
      role: 'Tanzlehrerin & Admin',
      img: '/assets/sophia.png',
    },
    {
      name: 'Amélie',
      role: 'Admin',
      img: '/assets/amelie.png',
    },
    {
      name: 'Flora Luvualu',
      role: 'Leitung Gesang',
      img: '/assets/flora.png',
    },
    {
      name: 'Akim Princes',
      role: 'Tanzpädagoge traditioneller Tanz',
      img: '/assets/akim.png',
    },
    {
      name: 'Yamoussa Sylla',
      role: 'Perkussionist',
      img: '/assets/yamoussa.png',
    },
    {
      name: 'Dramane Keita',
      role: 'Perkussionist',
      img: '/assets/dramane.png',
    },
    {
      name: 'Sahara Kuhn',
      role: 'Tanzlehrerin',
      img: '/assets/sahara.png',
    },
    {
      name: 'Altea Baumann',
      role: 'Tanzlehrerin',
      img: '/assets/altea.png',
    },
  ]

  let kids = [
    {
      name: 'Anisha',
      age: 14,
      origin: 'Angola / Südafrika',
      img: '/assets/anisha.png',
    },
    {
      name: 'Eleni',
      age: 12,
      origin: 'Griechenland / Jamaika / Schweiz',
      img: '/assets/eleni.png',
    },
    {
      name: 'Imani',
      age: 14,
      origin: 'Schweiz / Togo / Türkei',
      img: '/assets/imani.png',
    },
    {
      name: 'Imani',
      age: 14,
      origin: 'Belize / Brasilien / Schweiz',
      img: '/assets/imanii.png',
    },
    {
      name: 'Lena',
      age: 15,
      origin: 'Kamerun',
      img: '/assets/lena.png',
    },
    {
      name: 'Lionelle',
      age: 12,
      origin: 'Côte d’Ivoire / Schweiz',
      img: '/assets/lionelle.png',
    },
    {
      name: 'Sophie',
      age: 15,
      origin: 'Deutschland / Uganda',
      img: '/assets/sophie.png',
    },
    {
      name: 'Yaiza',
      age: 14,
      origin: 'Côte d’Ivoire / Schweiz',
      img: '/assets/yaiza.png',
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
          src="/assets/unseremission.png"
          alt="Unser Verein"
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
              src={kid.img}
              alt={kid.name}
              class="w-20 h-20 rounded-full object-cover shadow-md"
            />
            <h4 class="text-lg sm:text-xl md:text-2xl pt-2 text-red-500">
              {kid.name}
            </h4>
          </div>
          <p class="pl-2">{kid.age}, {kid.origin}</p>
        </div>
      {/each}
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
