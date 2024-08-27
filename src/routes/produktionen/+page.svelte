<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
</script>

<SectionWrapper>
  <Header />
  <div class="flex flex-col gap-10 flex-1 items-center mt-16">
    <!-- LE SOUFFLE - DIFF SLIDER TITLE -->
    <div
      class="diff aspect-[16/2] rounded-lg max-w-[1000px] mx-auto w-full text-center"
    >
      <div class="diff-item-1">
        <div
          class="bg-gray-100 text-xl lg:text-5xl md:text-3xl sm:text-2xl text-center grid place-content-center font-black font-semibold"
        >
          vom Hauch eines neuen Lebens
        </div>
      </div>
      <div class="diff-item-2">
        <div
          class="bg-black grid place-content-center text-5xl sm:text-6xl md:text-7xl text-white font-semibold"
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
        <img src="assets/ls1.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls2.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls3.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls4.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls5.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls6.png" alt="le souffle" />
      </div>
      <div class="carousel-item">
        <img src="assets/ls7.png" alt="le souffle" />
      </div>
    </div>
    <!-- PRODUCTION DESCRIPTION -->
    <div class="flex flex-col gap-2">
      <p class="text-base sm:text-lg md:text-xl text-justify max-w-[1000px]">
        <span class="text-red-500">Provokativ</span>,
        <span class="text-red-500">berührend</span>,
        <span class="text-red-500">wortlos</span>,
        <span class="text-red-500">witzig</span>. Das ist unsere jüngste
        Produktion namens
        <span class="text-red-500"
          >„Le Souffle – vom Hauch eines neuen Lebens“</span
        >. Sie geht eine brand-aktuelle Thematik an, die
        <span class="text-red-500">polarisiert</span>. Mit diesem Stück wagt
        sich CAL an <span class="text-red-500">sensitive Themen</span>, die den
        Nerv der Gesellschaft treffen und spricht dabei über Migration,
        Hoffnung, Fremdenhass, Integration, Mischlingskinder und Liebe. Das
        Stück handelt vom Aufbruch in eine neue, hoffentlich bessere Welt, den
        zahlreiche Migrantinnen und Migranten wagen.
      </p>
      <p class="text-base sm:text-lg md:text-xl text-justify max-w-[1000px]">
        Die anfängliche Freude, aber auch die Gefahren und Trauer auf diesem Weg
        werden von CALs Nachwuchstalenten sowie von professionellen Tänzern
        Afrikas mit <span class="text-red-500">farbenfrohen Kostümen</span>,
        <span class="text-red-500">atemberaubenden Tänzen</span>, pulsierenden
        Trommeln und betörenden Gesängen dargestellt. Ein Muss für Liebhaber des
        traditionellen und zeitgenössischen afrikanischen Tanzes und alle, die
        ihren Horizont erweitern wollen.
      </p>
    </div>

    <!-- RECENT EXHIBITIONS -->
    <div class="flex flex-col gap-2">
      <p
        class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
      >
        <span>Recent features</span>
      </p>
    </div>
    <div
      class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4 max-w-[1000px]"
    >
      <div class="card glass w-full">
        <figure>
          <img src="assets/caliente2024.png" alt="car!" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Life hack</h2>
          <p>How to park your car at your garage?</p>
        </div>
      </div>
      <div class="card glass w-full">
        <figure>
          <img src="assets/asj2024.png" alt="car!" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Life hack</h2>
          <p>How to park your car at your garage?</p>
        </div>
      </div>
      <div class="card glass w-full">
        <figure>
          <img src="assets/zts2022.png" alt="car!" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Life hack</h2>
          <p>How to park your car at your garage?</p>
        </div>
      </div>
      <div class="card glass w-full">
        <figure>
          <img
            src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
            alt="car!"
          />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Life hack</h2>
          <p>How to park your car at your garage?</p>
        </div>
      </div>
      <div class="card glass w-full">
        <figure>
          <img
            src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
            alt="car!"
          />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Life hack</h2>
          <p>How to park your car at your garage?</p>
        </div>
      </div>
    </div>
  </div></SectionWrapper
>
<Footer />
