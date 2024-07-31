<script>
  import SectionWrapper from '../../components/SectionWrapper.svelte'
</script>

<SectionWrapper>
  <div
    class="relative flex flex-col w-full mb-20 mt-20 shadow-lg rounded-lg max-w-[800px] mx-auto bg-[#FFF1DB]"
  >
    <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
      <form>
        <h6
          class="text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
        >
          Anmeldung
        </h6>
        <h6 class="mt-3 mb-6 font-bold uppercase">Kind</h6>
        <div class="flex flex-wrap">
          <div class="w-full lg:w-6/12 px-4">
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
          <div class="w-full lg:w-6/12 px-4">
            <div class="relative w-full mb-3">
              <label class="block text-sm font-semibold mb-2" for="grid-email">
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
                Herkunft (bei mehreren bitte alle angeben. Wird ausschliesslich
                zu statistischen Zwecken verwendet)
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
        <h6 class="mt-3 mb-6 font-bold uppercase">Erziehungsberechtigte:r 1</h6>
        <div class="flex flex-wrap">
          <div class="w-full lg:w-12/12 px-4">
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
          <div class="w-full px-4">
            <div class="relative w-full mb-3">
              <label class="block text-sm font-semibold mb-2" for="grid-city">
                Strasse, Nr, PLZ, Ort <span class="text-red-500">*</span>
              </label>
              <div class="grid grid-cols-1 mb-4">
                <!-- Strasse input field -->
                <input
                  id="grid-strasse"
                  type="text"
                  placeholder="Strasse"
                  class="col-span-1 lg:col-span-4 md:col-span-4 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  required
                />
              </div>
              <div class="grid grid-cols-3 lg:grid-cols-3 gap-4">
                <!-- Nr input field -->
                <input
                  id="grid-nr"
                  type="text"
                  placeholder="Nr"
                  class="col-span-1 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  required
                />
                <!-- PLZ input field -->
                <input
                  id="grid-plz"
                  type="text"
                  placeholder="PLZ"
                  class="col-span-1 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  required
                />
                <!-- Ort input field -->
                <input
                  id="grid-ort"
                  type="text"
                  placeholder="Ort"
                  class="col-span-1 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  required
                />
              </div>
            </div>
          </div>

          <div class="w-full px-4">
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
          <div class="w-full px-4">
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
        </div>

        <!-- legal guardian 2 -->
        <h6 class="mt-3 mb-6 font-bold uppercase">Erziehungsberechtigte:r 2</h6>
        <div class="flex flex-wrap">
          <div class="w-full lg:w-12/12 px-4">
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
          <div class="w-full lg:w-4/12 px-4">
            <div class="relative w-full mb-3">
              <label class="block text-sm font-semibold mb-2" for="grid-city">
                Strasse, Nr, PLZ, Ort
              </label>
              <div class="grid grid-cols-1 lg:grid-cols-4 gap-4">
                <!-- Strasse input field -->
                <input
                  id="grid-strasse"
                  type="text"
                  placeholder="Strasse"
                  class="col-span-1 lg:col-span-4 md:col-span-4 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                />
                <!-- Nr input field -->
                <input
                  id="grid-nr"
                  type="text"
                  placeholder="Nr"
                  class="col-span-1 lg:col-span-1 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                />
                <!-- PLZ input field -->
                <input
                  id="grid-plz"
                  type="text"
                  placeholder="PLZ"
                  class="col-span-1 lg:col-span-1 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                />
                <!-- Ort input field -->
                <input
                  id="grid-ort"
                  type="text"
                  placeholder="Ort"
                  class="col-span-1 lg:col-span-2 border-0 px-3 py-3 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                />
              </div>
            </div>
          </div>

          <div class="w-full lg:w-4/12 px-4">
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
          <div class="w-full lg:w-4/12 px-4">
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
        </div>

        <!-- buttons -->
        <div class="flex items-center gap-4 justify-center pt-10">
          <button class={'specialBtnDark'}>
            <p class="text-base sm:text-lg md:text-xl">Senden</p>
          </button>

          <a href="/">
            <button class="specialBtn">
              <p class="text-base sm:text-lg md:text-xl">Abbrechen</p>
            </button>
          </a>
        </div>
      </form>
    </div>
  </div>
</SectionWrapper>
