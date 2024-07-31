<script>
  import '../app.css'
  import CtAs from '../components/CTAs.svelte'
  import Header from '../components/Header.svelte'

  import { openModal } from '../store'

  let y
  $: outerHeight = 0

  function reroute(href) {
    $openModal = false
    window.location.href = href
  }
</script>

{#if $openModal}
  <div
    class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 p-5 px-8 md:hidden"
  >
    <!-- mobile screen navbar burger menu -->
    <div class="flex items-center justify-between gap-4 border-b pb-2">
      <a href="/" class="flex items-center">
        <img alt="The project logo" src="/assets/logo.png" class="w-12 h-12" />
        <h1 class="font-semibold ml-2">Café au Lait</h1>
      </a>
      <button
        on:click={() => ($openModal = false)}
        class="outline-none border-none"
      >
        <i class="fa-solid fa-xmark text-2xl"></i>
      </button>
    </div>

    <!-- mobile burger menu options to click -->
    <div class="flex flex-col gap-4 flex-1">
      <button
        on:click={() => reroute('/')}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          <i class="fa-solid fa-chevron-right text-xl pl-4" /> Home
        </p>
      </button>
      <button
        on:click={() => reroute('#kurse')}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          <i class="fa-solid fa-chevron-right text-xl pl-4" /> Kurse
        </p>
      </button>
      <button
        on:click={() => reroute('#shows')}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          <i class="fa-solid fa-chevron-right text-xl pl-4" /> Shows
        </p>
      </button>
      <button
        on:click={() => reroute('#uberuns')}
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
      >
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
          <i class="fa-solid fa-chevron-right text-xl pl-4" /> Über Uns
        </p>
      </button>
    </div>
    <div class="flex flex-col items-center justify-center">
      <CtAs />
    </div>
  </div>
{/if}

{#if y > outerHeight}
  <div
    class="bg-white fixed top-0 left-0 w-full flex flex-col z-20 px-4 fadeIn"
  >
    <Header />
  </div>
{/if}
<slot />
<svelte:window bind:scrollY={y} bind:outerHeight />
