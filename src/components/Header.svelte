<script>
  import { goto } from '$app/navigation'
  import { openModal } from '../store'

  function navigateToSection(sectionId) {
    const isHomePage = window.location.pathname === '/'

    if (!isHomePage) {
      goto('/')

      setTimeout(() => {
        const section = document.getElementById(sectionId)
        if (section) {
          section.scrollIntoView({ behavior: 'smooth' })
        }
      }, 300)
    } else {
      const section = document.getElementById(sectionId)
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' })
      }
    }
  }
</script>

<header class="flex flex-col relative z-20">
  <div
    class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6"
  >
    <a href="/" class="flex items-center">
      <img
        alt="The project logo"
        src="/assets/pics/logo.png"
        class="w-12 h-12"
      />
      <h1 class="font-semibold ml-2">Café au Lait</h1>
    </a>
    <a
      href="https://www.stadt-zuerich.ch/de/aktuell/medienmitteilungen/2023/10/231024a2.html"
      target="_blank"
      class="flex items-center transition-transform duration-300 hover:scale-110"
    >
      <img
        src="/assets/pics/zuri.png"
        alt="zuri"
        class="w-16 sm:w-20 md:w-20 lg:w-20"
      />
      <p>Kulturelle Auszeichnungen der Stadt Zürich 2023</p>
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
      <a
        href="#kurse"
        class="duration-200 hover:text-red-500 cursor-pointer"
        on:click|preventDefault={() => navigateToSection('kurse')}
      >
        Kurse
      </a>
      <a
        href="#shows"
        class="duration-200 hover:text-red-500 cursor-pointer"
        on:click|preventDefault={() => navigateToSection('shows')}
      >
        Shows
      </a>
      <a href="mailto:info@cafeaulait.ch">
        <button class="specialBtn">
          <p>Kontakt</p>
        </button>
      </a>
    </nav>
  </div>
</header>
