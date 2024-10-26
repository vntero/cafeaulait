<script>
  import SectionWrapper from '../components/SectionWrapper.svelte'
  import { createEventDispatcher } from 'svelte'
  import handleSubmit from '../components/BookModal.svelte'
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
        <!-- x button to close window -->
        <button
          class="absolute top-4 right-4 text-gray-600 hover:text-gray-800"
          on:click={close}
        >
          <i class="fa-solid fa-xmark text-xl"></i>
        </button>
        <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
          <form
            on:submit={(e) => handleSubmit(e, 'http://localhost:8080/register')}
          >
            <h6
              class="text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
            >
              Anmeldung
              <!-- Add space and edit font size and color to "normal" text for the following text -->
              Bist du an einem Schnuppertraining interessiert? Schreib uns unter
              info@cafeaulait.ch und wir sagen dir, wann das näcshte Schnuppertraining
              stattfindet.
            </h6>

            <!-- child -->
            <h6 class="mt-3 mb-6 font-bold uppercase">Kind</h6>
            <div class="flex flex-wrap">
              <div class="w-6/12 lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="register-name"
                  >
                    Name, Vorname <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="register-name"
                    name="name"
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
                    for="register-birthday"
                  >
                    Geburtsdatum <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="register-birthday"
                    name="birthday"
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
                    for="register-origin"
                  >
                    Herkunft (bei mehreren bitte alle angeben. Wird
                    ausschliesslich zu statistischen Zwecken verwendet)
                  </label>
                  <input
                    id="register-origin"
                    name="origin"
                    type="text"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
              <div class="w-full lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="register-motivation"
                  >
                    Motivationsgrund für die Anmeldung sowie allfällige
                    tänzerische/sportliche Erfahrung
                  </label>
                  <textarea
                    id="register-motivation"
                    name="motivation"
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
              Erziehungsberechtigte:r 1
            </h6>
            <div class="flex flex-wrap">
              <div class="w-6/12 md:w-5/12 lg:w-5/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block text-sm font-semibold mb-2"
                    for="register-parent-one-name"
                  >
                    Name, Vorname <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="register-parent-one-name"
                    name="parent_one_name"
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
                    for="register-parent-one-email"
                  >
                    E-mail <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="register-parent-one-email"
                    name="parent_one_email"
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
                    for="register-parent-one-tel"
                  >
                    Telefonnr. <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="register-parent-one-tel"
                    name="parent_one_phone"
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
                    name="parent_one_street"
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
                    for="grid-house-number"
                  >
                    Nr <span class="text-red-500">*</span>
                  </label>
                  <input
                    id="grid-house-number"
                    name="parent_one_house_number"
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
                    name="parent_one_postcode"
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
                    name="parent_one_location"
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
                    name="parent_two_name"
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
                    name="parent_two_email"
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
                    name="parent_two_phone"
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
                    name="parent_two_street"
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
                    name="parent_two_house_number"
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
                    name="parent_two_postcode"
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
                    name="parent_two_location"
                    type="tel"
                    class="border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  />
                </div>
              </div>
            </div>

            <!-- checkbox -->
            <div class="flex items-center justify-center pt-10">
              <input
                type="checkbox"
                id="terms"
                name="terms"
                required
                class="checkbox bg-white mr-2 border-black"
              />
              <label for="terms" class="text-sm font-semibold">
                Ich akzeptiere die <a href="/t&c" class="underline"
                  >Allgemeinen Bestimmungen</a
                >
              </label> <span class="text-red-500 text-sm ml-1">*</span>
            </div>

            <!-- buttons -->
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
