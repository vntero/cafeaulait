<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-10 flex-1 items-center mt-16">
    <!-- SLIDER TITLE -->
    <div
      class="diff aspect-[16/2] rounded-lg max-w-[1000px] mx-auto w-full text-center"
    >
      <div class="diff-item-1">
        <div
          class="bg-gray-500 text-primary-content grid place-content-center text-5xl sm:text-6xl md:text-7xl font-black font-semibold"
        >
          Le Souffle
        </div>
      </div>
      <div class="diff-item-2">
        <div
          class="bg-base-200 grid place-content-center text-5xl sm:text-6xl md:text-7xl font-black font-semibold"
        >
          Le Souffle
        </div>
      </div>
      <div class="diff-resizer"></div>
    </div>

    <!-- SHORT DESCRIPTION AND PRODUCER -->
    <div class="flex flex-col gap-2">
      <p
        class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
      >
        <span class="italic">"Le Souffle" - vom Hauch eines neuen Lebens</span>
      </p>
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Eine Produktion von <span class="text-red-500"
          >Françoise Strassburg</span
        >
      </p>
    </div>

    <!-- CAROUSEL -->
    <div class="carousel rounded-box space-x-2 h-64 max-w-[1000px]">
      <div class="carousel-item">
        <img src="assets/ls1.png" alt="Burger" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls2.png" alt="Burger" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls3.png" alt="Burger" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls4.png" alt="Burger" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls5.png" alt="Burger" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls6.png" alt="Burger" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls7.png" alt="Burger" />
      </div>
    </div>
    <!-- PRODUCTION DESCRIPTION -->
  </div></SectionWrapper
>
<Footer />
