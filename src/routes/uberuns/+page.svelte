<script>
  import SectionWrapper from './SectionWrapper.svelte'
  let faqs = [
    {
      question: 'What is Swoley Moley?',
      ans: 'Swoley Moley is a fun fitness app designed to make your workouts enjoyable by incorporating interactive games and challenges.',
    },
    {
      question: 'How do I download Swoley Moley?',
      ans: 'You can download Swoley Moley from the App Store (for iOS) or Google Play Store (for Android) on your mobile device.',
    },
    {
      question: 'Is Swoley Moley free to use?',
      ans: 'Yes, Swoley Moley offers a free version with basic features. There is also a premium subscription that unlocks additional games and advanced workout tracking.',
    },
    {
      question: 'What types of workouts does Swoley Moley offer?',
      ans: 'Swoley Moley offers a variety of workouts, including cardio, strength training, and flexibility exercises. The workouts are designed to be engaging and entertaining.',
    },
    {
      question: 'Can I connect Swoley Moley to my fitness tracker?',
      ans: 'Yes, Swoley Moley supports integration with popular fitness trackers, allowing you to sync your workout data and track your progress seamlessly.',
    },
    {
      question: 'Are there multiplayer features in Swoley Moley?',
      ans: 'Yes, Swoley Moley includes multiplayer challenges, allowing you to compete with friends or join group workouts for a more interactive and social experience.',
    },
    {
      question: 'How does Swoley Moley motivate users to stay active?',
      ans: 'Swoley Moley employs a reward system, where users earn points and achievements for completing workouts. These rewards can be used to unlock new levels, challenges, and in-app content.',
    },
    {
      question: 'Can I customize my workouts in Swoley Moley?',
      ans: 'Absolutely! Swoley Moley allows users to customize their workouts based on personal preferences, fitness goals, and available equipment.',
    },
    {
      question: 'Is there a beginner-friendly mode in Swoley Moley?',
      ans: 'Yes, Swoley Moley offers a beginner-friendly mode with easier exercises and lower intensity workouts, making it suitable for users at various fitness levels.',
    },
    {
      question: 'How often should I use Swoley Moley for optimal results?',
      ans: 'The frequency of Swoley Moley workouts depends on your fitness goals. It is recommended to engage in at least 3-5 sessions per week for noticeable results.',
    },
  ]
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

<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        For all your questions, qualms & queries
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Frequently Asked Questions
      </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">
            {faq.question}
          </h4>
          <p class="pl-2">{faq.ans}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
