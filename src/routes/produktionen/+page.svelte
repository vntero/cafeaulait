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
          <img src="assets/pics/revolution.png" alt="R'Evolution" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">
            R'Evolution
            <div class="badge badge-secondary">COMING SOON</div>
          </h2>
          <p>
            Café au Lait feiert dieses Jahr ihr 20-jähriges Bestehen. Anlässlich
            dieses Ereignisses stellt sie ihre jüngste Produktion vor und
            erzählt dabei eine Geschichte, die niemanden kalt lässt.
          </p>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="card w-96 shadow-xl">
        <figure>
          <img src="assets/pics/lesouffle.png" alt="Le Souffle" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Le Souffle - 2018</h2>
          <p>
            Die Geschichte beginnt in Afrika vor sehr langer Zeit. Die Menschen
            leben bescheiden, der Rhythmus begleitet sie durch den friedlichen
            Alltag. Eines Tages wird das Dorfleben plötzlich auf den Kopf
            gestellt. Besuch aus Europa steht vor der Tür. Der Reichtum ruft und
            Aufregung macht sich unter den Dorfbewohnern breit. Sollen sie
            aufbrechen oder bleiben?
          </p>
          <div class="card-actions justify-end mt-3">
            <a href="/lesouffle"
              ><button class="specialBtnDark">Mehr erfahren</button></a
            >
          </div>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="card w-96 shadow-xl">
        <figure>
          <img src="assets/pics/queenleoni.png" alt="Queen Leoni" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Queen Leoni - 20XX</h2>
          <p>Lorem Ipsum.</p>
          <div class="card-actions justify-end mt-3">
            <a href="/queenleoni"
              ><button class="specialBtnDark">Mehr erfahren</button></a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</SectionWrapper>
<Footer />
