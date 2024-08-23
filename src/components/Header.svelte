<script>
  import { openModal } from '../store'
</script>

<header class="flex flex-col relative z-20">
  <div
    class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6"
  >
    <a href="/" class="flex items-center">
      <img alt="The project logo" src="/assets/logo.png" class="w-12 h-12" />
      <h1 class="font-semibold ml-2">Café au Lait</h1>
    </a>
    <button
      on:click={() => ($openModal = true)}
      class="md:hidden grid place-items-center"
    >
      <i class="fa-solid fa-bars"></i>
    </button>
    <nav class="hidden md:flex items-center gap-4 lg:gap-6">
      <a href="/" class="duration-200 hover:text-red-500 cursor-pointer">Home</a
      >
      <a href="#kurse" class="duration-200 hover:text-red-500 cursor-pointer"
        >Kurse</a
      >
      <a href="#shows" class="duration-200 hover:text-red-500 cursor-pointer"
        >Shows</a
      >
      <a href="mailto:info@cafeaulait.ch">
        <button class="specialBtn">
          <p>Kontakt</p>
        </button>
      </a>
    </nav>
  </div>
</header>
