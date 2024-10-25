<script>
  import SectionWrapper from '../components/SectionWrapper.svelte'
  import { createEventDispatcher } from 'svelte'

  const dispatch = createEventDispatcher()

  export let show = true
  export let close = () => {
    show = false
    dispatch('close')
  }

  // function to handle form submission via http request
  export const handleSubmit = async (event, url) => {
    event.preventDefault() // prevent default form submission behaviour

    const formData = new FormData(event.target)
    const data = Object.fromEntries(formData)

    try {
      const response = await fetch(url, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify(data),
      })

      if (response.ok) {
        // Handle successful response
        console.log('Form submitted successfully')
        // Optionally close the modal or show a success message
        close()
      } else {
        // Handle error response
        const errorData = await response.json()
        console.error('Form submission failed:', errorData)
      }
    } catch (error) {
      console.error('Error submitting form:', error)
    }
  }
</script>

{#if show}
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-no-static-element-interactions -->
  <div
    class="fixed pb-10 inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50"
    on:click={close}
  >
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <SectionWrapper>
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-static-element-interactions -->
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
          <form
            on:submit={(e) => handleSubmit(e, 'http://localhost:8080/book')}
          >
            <h6
              class="text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
            >
              Show buchen
            </h6>
            <br />
            <p>
              Interessiert an einer Show? Fülle das Formular aus und wir melden
              uns bei dir.
            </p>
            <!-- CONTACT DETAILS -->
            <h6 class="mt-3 mb-6 font-bold uppercase">Kontaktdaten</h6>
            <div class="flex flex-wrap">
              <div class="w-full lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="contact-name"
                  >
                    Vor- und Nachname <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="name"
                    name="name"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>
              <div class="w-full lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label class="block text-sm font-semibold mb-2" for="phone">
                    Telefonnummer <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="phone"
                    name="phone"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>
              <div class="w-full lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label class="block text-sm font-semibold mb-2" for="email">
                    Emailadresse <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="email"
                    name="email"
                    type="email"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>
              <div class="w-full lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label class="block text-sm font-semibold mb-2" for="email">
                    Organisation
                  </label>
                  <input
                    id="email"
                    name="email"
                    type="email"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
            </div>
            <!-- BOOKING DETAILS -->
            <h6 class="mt-3 mb-6 font-bold uppercase">Veranstaltungsdetails</h6>
            <div class="flex flex-wrap">
              <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="location"
                  >
                    Veranstaltungsort
                  </label>
                  <input
                    id="location"
                    name="location"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="duration"
                  >
                    Gewünschte Dauer der Darbietung
                  </label>
                  <input
                    id="duration"
                    name="duration"
                    type="number"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label class="block text-sm font-semibold mb-2" for="guests">
                    Gästeanzahl
                  </label>
                  <input
                    id="guests"
                    name="number_of_guests"
                    type="number"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="event-date"
                  >
                    Veranstaltungsdatum
                  </label>
                  <input
                    id="event-date"
                    name="event_date"
                    type="date"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="event-time"
                  >
                    Veranstaltungszeit
                  </label>
                  <input
                    id="event-time"
                    name="event_time"
                    type="time"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label class="block text-sm font-semibold mb-2" for="budget">
                    Budget
                  </label>
                  <input
                    id="budget"
                    name="budget"
                    type="number"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
            </div>

            <!-- ADDITIONAL INFORMATION -->
            <h6 class="mt-3 mb-6 font-bold uppercase">
              Zusätzliche Informationen
            </h6>
            <div class="flex flex-wrap">
              <div class="w-full px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="additional-comments"
                  >
                    Zusätzliche Infos oder Fragen
                  </label>
                  <textarea
                    id="additional-comments"
                    name="comment"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    rows="4"
                  />
                </div>
              </div>
            </div>

            <div class="flex items-center gap-4 justify-center pt-10">
              <button type="submit" class="specialBtnDark">
                <p class="text-base sm:text-lg md:text-xl">Senden</p>
              </button>

              <button class="specialBtnCancel" on:click={close}>
                <p class="text-base sm:text-lg md:text-xl">Abbrechen</p>
              </button>
            </div>
          </form>
        </div>
      </div>
    </SectionWrapper>
  </div>
{/if}
