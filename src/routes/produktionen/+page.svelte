<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-2 mt-20">
    <p class="opacity-60 text-base sm:text-lg md:text-xl text-center"></p>
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
      <div class="card w-96 shadow-xl">
        <figure>
          <img src="assets/revolution.png" alt="R'Evolution" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">
            R'Evolution
            <div class="badge badge-secondary">COMING SOON</div>
          </h2>
          <p>
          Begleitet von einem Chor und emotionalen Tanzeinlagen, erzählt dieses Stück 
          die Geschichte von Frauen und ihrem Weg durch gesellschaftliche und persönliche Hürden. 
          Lass dich berühren und inspirieren und erlebe eine Aufführung, die bewegt und Debatten anstößt          </p>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="card w-96 shadow-xl">
        <figure>
          <img src="assets/lesouffle.png" alt="Le Souffle" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Le Souffle - 2018</h2>
          <p>
            Provokativ, berührend, wortlos, witzig. Das ist die Produktion namens 
            „Le Souffle – vom Hauch eines neuen Lebens“. Sie geht eine brandaktuelle Thematik an, 
            die bewegt und den Nerv der Gesellschaft trifft. Das Stück handelt vom Aufbruch 
            in eine neue, hoffentlich bessere Welt, den zahlreiche Migrantinnen und Migranten wagen.
          </p>
          <div class="card-actions justify-end mt-3">
            <a href="/lesouffle"
              >
              <button class="specialBtnDark">Mehr erfahren</button></a>
          </div>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="card w-96 shadow-xl">
        <figure>
          <img src="assets/queenleoni.png" alt="Queen Leoni" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Diverse Produktionen - Seit 2004</h2>
          <p>
            Café au Lait erarbeitet bereits seit seinem Bestehen Showeinlagen.
            Seit 2011 kommen Musical-Märchen wie etwa "Zango" und 2015 "Queen Leonie" dazu.
          </p>
          <!-- <div class="card-actions justify-end mt-3">
            <a href="/queenleoni"
              ><button class="specialBtnDark">Mehr erfahren</button></a
            >
          </div> -->
        </div>
      </div>
    </div>
  </div>
</SectionWrapper>
<Footer />
