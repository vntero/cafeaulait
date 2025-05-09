<script>
  import SectionWrapper from '../components/SectionWrapper.svelte'
  import { createEventDispatcher } from 'svelte'

  const dispatch = createEventDispatcher()

  export let show = true
  export let close = () => {
    show = false
    dispatch('close')
  }

  // Add message state
  let message = null

  // Updated submit handler with message handling
  // const handleSubmitBook = async (event, url) => {
  //   event.preventDefault()

  //   const formData = new FormData(event.target)
  //   const data = Object.fromEntries(formData)

  //   try {
  //     const response = await fetch(url, {
  //       method: 'POST',
  //       headers: {
  //         'Content-Type': 'application/json',
  //       },
  //       body: JSON.stringify(data),
  //     })

  //     if (response.ok) {
  //       message = {
  //         type: 'success',
  //         text: 'Buchungsanfrage erfolgreich gesendet!',
  //       }
  //       // Close modal after delay
  //       setTimeout(() => {
  //         close()
  //       }, 2000)
  //     } else {
  //       const errorData = await response.text()
  //       message = { type: 'error', text: `Fehler: ${errorData}` }
  //       setTimeout(() => {
  //         message = null
  //       }, 5000)
  //     }
  //   } catch (error) {
  //     message = {
  //       type: 'error',
  //       text: `Netzwerkfehler: ${error.message}. Bitte versuchen Sie es erneut.`,
  //     }
  //     setTimeout(() => {
  //       message = null
  //     }, 5000)
  //   }
  // }
</script>

{#if show}
  <button
    class="fixed pb-10 inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50"
    on:click={close}
    on:keydown={(e) => e.key === 'Escape' && close()}
    aria-label="Close modal"
    role="button"
  >
    <SectionWrapper>
      <div
        class="relative flex flex-col w-full mb-6 shadow-lg rounded-lg max-w-[1000px] mx-auto m-20 bg-[#FFF1DB] max-h-screen overflow-y-auto"
        on:click|stopPropagation
      >
        <!-- x button to close window -->
        <button
          class="absolute top-4 right-4 text-gray-600 hover:text-gray-800"
          on:click={close}
        >
          <i class="fa-solid fa-xmark text-xl"></i>
        </button>
        <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
          <!-- Title -->
          <h6
            class="text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
          >
            15. Juni Premiere "R’Evolution"
          </h6>
          <!-- Tickets Link -->
          <a
            href="https://eventfrog.ch/de/p/musicals-shows/musical/revolution-keine-revolution-ohne-frauen-7322282210823823399.html"
            class="block text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6 hover:text-black cursor-pointer duration-200"
            target="_blank"
            rel="noopener noreferrer"
          >
            <u>Tickets hier kaufen</u>
          </a>
          <!-- Revolution Image -->
          <div class="flex justify-center mt-10">
            <img
              src="/assets/pics/revolution.png"
              alt="Revolution"
              class="w-full max-w-[800px] rounded-lg shadow-md"
            />
          </div>
        </div>
      </div>
    </SectionWrapper>
  </button>
{/if}
