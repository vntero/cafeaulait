<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-2 mt-20">
    <h3
      class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
    >
      Unsere <span class="text-red-500">Produktionen</span>
    </h3>
  </div>
  <div class="flex flex-col gap-10 flex-1 mt-16">
    <!-- Container for horizontal card layout -->
    <div class="flex flex-wrap justify-center gap-10">
      <!-- Card 1 -->
      <div
        class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300 overflow-hidden"
      >
        <img
          src="assets/pics/revolution.png"
          alt="R'Evolution"
          class="w-full h-48 object-cover"
        />
        <div class="p-6">
          <h2 class="text-2xl font-semibold mb-2">R'Evolution - 2025</h2>
          <p class="text-gray-700 mb-4">
            Begleitet von einem Chor und emotionalen Tanzeinlagen erzählt dieses
            Stück die Geschichte von Frauen und ihrem Weg durch
            gesellschaftliche und persönliche Hürden. Lass dich berühren und
            inspirieren und erlebe eine Aufführung, die bewegt und Debatten
            anstösst.
          </p>
        </div>
      </div>

      <!-- Card 2 -->
      <div
        class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300 overflow-hidden"
      >
        <img
          src="assets/pics/lesouffle.png"
          alt="Le Souffle"
          class="w-full h-48 object-cover"
        />
        <div class="p-6">
          <h2 class="text-2xl font-semibold mb-2">Le Souffle - 2018</h2>
          <p class="text-gray-700 mb-4">
            Provokativ, herzzerreissend, wortlos und manchmal lustig. Das ist
            die Produktion „Le Souffle – vom Hauch eines neuen Lebens“. Das
            Stück geht unter die Haut und handelt von Menschen, die den Aufbruch
            in eine neue, hoffnungsvollere Welt wagen.
          </p>
          <a
            href="/lesouffle"
            class="inline-block text-white bg-red-500 px-4 py-2 rounded-lg hover:bg-red-600 transition-colors"
          >
            Mehr erfahren
          </a>
        </div>
      </div>

      <!-- Card 3 -->
      <div
        class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300 overflow-hidden"
      >
        <img
          src="assets/pics/queenleoni.png"
          alt="Queen Leoni"
          class="w-full h-48 object-cover"
        />
        <div class="p-6">
          <h2 class="text-2xl font-semibold mb-2">
            Diverse Produktionen - Seit 2004
          </h2>
          <p class="text-gray-700 mb-4">
            Wir erarbeiten schon seit unserem Bestehen Showeinlagen. Seit 2011
            kommen Musical-Märchen wie etwa "Zango" und 2015 "Queen Leonie"
            dazu.
          </p>
        </div>
      </div>
    </div>
  </div>
</SectionWrapper>
<Footer />
