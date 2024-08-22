<script>
  import SectionWrapper from '../components/SectionWrapper.svelte'
  import { createEventDispatcher } from 'svelte'
  const dispatch = createEventDispatcher()
  export let show = true
  export let close = () => {
    show = false
    dispatch('close')
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
        <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
          <form>
            <h6
              class="text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
            >
              Anmeldung
            </h6>

            <!-- child -->
            <h6 class="mt-3 mb-6 font-bold uppercase">
              Kind <span class="text-red-500">*</span>
            </h6>
            <div class="flex flex-wrap">
              <div class="w-6/12 lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-username"
                  >
                    Name, Vorname <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-username"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>
              <div class="w-6/12 lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-email"
                  >
                    Geburtsdatum <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-email"
                    type="date"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>
              <div class="w-full lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-first-name"
                  >
                    Herkunft (bei mehreren bitte alle angeben. Wird
                    ausschliesslich zu statistischen Zwecken verwendet)
                  </label>
                  <input
                    id="grid-first-name"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-last-name"
                  >
                    Motivationsgrund für die Anmeldung sowie allfällige
                    tänzerische/sportliche Erfahrung
                  </label>
                  <textarea
                    id="grid-about-me"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    rows="4"
                  />
                </div>
              </div>
            </div>

            <hr class="mt-6 border-b-1 border-blueGray-300" />
            <br />

            <!-- legal guardian 1 -->
            <h6 class="mt-3 mb-6 font-bold uppercase">
              Erziehungsberechtigte:r 1 <span class="text-red-500">*</span>
            </h6>
            <div class="flex flex-wrap">
              <div class="w-6/12 md:w-5/12 lg:w-5/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-address"
                  >
                    Name, Vorname <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-address"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-4/12 lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-country"
                  >
                    E-mail <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-country"
                    type="email"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-3/12 lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Telefonnr. <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-5/12 lg:w-5/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Strasse <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-postal-code"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>

              <div class="w-3/12 md:w-2/12 lg:w-2/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Nr <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>

              <div class="w-3/12 md:w-2/12 lg:w-2/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    PLZ <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-3/12 lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Ort <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    required
                  />
                </div>
              </div>
            </div>

            <!-- legal guardian 2 -->
            <h6 class="mt-3 mb-6 font-bold uppercase">
              Erziehungsberechtigte:r 2
            </h6>
            <div class="flex flex-wrap">
              <div class="w-6/12 md:w-5/12 lg:w-5/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-address"
                  >
                    Name, Vorname
                  </label>
                  <input
                    id="grid-address"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-4/12 lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-country"
                  >
                    E-mail
                  </label>
                  <input
                    id="grid-country"
                    type="email"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-3/12 lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Telefonnr.
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-5/12 lg:w-5/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Strasse
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>

              <div class="w-3/12 md:w-2/12 lg:w-2/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Nr
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>

              <div class="w-3/12 md:w-2/12 lg:w-2/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    PLZ
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>

              <div class="w-6/12 md:w-3/12 lg:w-3/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="grid-postal-code"
                  >
                    Ort
                  </label>
                  <input
                    id="grid-postal-code"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
            </div>

            <!-- buttons -->
            <div class="flex items-center gap-4 justify-center pt-10">
              <button class="specialBtnDark">
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
