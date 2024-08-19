<script>
  import Header from '../../components/Header.svelte'
  import Footer from '../../components/Footer.svelte'
</script>

<!-- <Header /> -->
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
  <a href="/">
    <button class={'specialBtnCancel'}>
      <p class="text-base sm:text-lg md:text-xl">Zurück zur Startseite</p>
    </button>
  </a>
</div>
<!-- <Footer /> -->
