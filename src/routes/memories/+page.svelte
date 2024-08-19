<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-10 flex-1 items-center justify-center">
    <p
      class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
    >
      <span class="italic"
        >Diese Seite ist derzeit <span class="text-red-500"
          >in Bearbeitung...</span
        ></span
      >
    </p>
    <!--
    <section class="block relative z-1 bg-blueGray-600">
      <div class="container mx-auto">
        <div class="justify-center flex flex-wrap">
          <div class="w-full lg:w-12/12 px-4 -mt-24">
            <div class="flex flex-wrap">
              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">
                  Afropfingsten - 18.05.2020
                </h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/Afropfingsten - 18.05.2020/CAL Afropfingesten 2018_10430.jpg"
                    />
                  </div>
                </a>
              </div>

              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">
                  FIFA Family Day - 30.08.2019
                </h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/FIFA Family Day - 30.08.2019/_DSC0547.JPG"
                    />
                  </div>
                </a>
              </div>

              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">
                  Le Souffle - 19.08.2024
                </h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/Le Souffle Kids - 19.08.2024/051-CAL 18 Le Souffle with Dancers - 180317_144356 - (c) fototscharner.ch051.jpg"
                    />
                  </div>
                </a>
              </div>
            </div>
          </div>

          <div class="w-full lg:w-12/12 px-4">
            <div class="flex flex-wrap">
              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">
                  Portraits session - 19.09.2024
                </h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/Portraits session - 19.09.2024/portraits cover.png"
                    />
                  </div>
                </a>
              </div>

              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">
                  Volkshaus - 28.06.2016
                </h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/Volkshaus - 28.06.2016/bild_24.jpg"
                    />
                  </div>
                </a>
              </div>

              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">Album 6</h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/afrotanz.png"
                    />
                  </div>
                </a>
              </div>
            </div>
          </div>
          <div class="w-full lg:w-12/12 px-4">
            <div class="flex flex-wrap">
              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">Album 7</h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/afrotanz.png"
                    />
                  </div>
                </a>
              </div>

              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">Album 8</h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/afrotanz.png"
                    />
                  </div>
                </a>
              </div>

              <div class="w-full lg:w-4/12 px-4">
                <h5 class="text-xl font-semibold pb-4 text-center">Album 9</h5>
                <a href="/">
                  <div
                    class="hover:-mt-4 relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg ease-linear transition-all duration-150"
                  >
                    <img
                      alt="..."
                      class="align-middle border-none max-w-full h-auto rounded-lg"
                      src="assets/afrotanz.png"
                    />
                  </div>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  -->
  </div>
  <Footer />
</SectionWrapper>
