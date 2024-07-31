<div
  class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg bg-blueGray-100 border-0"
>
  <!-- <div
      class="max-w-[1000px] mx-auto w-full text-center bg-[#FFF1DB] p-6 rounded-lg shadow-lg"
    > -->
  <div class="rounded-t bg-white mb-0 px-6 py-6">
    <div class="text-center">
      <h6 class="text-red-500 text-xl font-bold">Anmeldung</h6>
    </div>
  </div>

  <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
    <form>
      <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
        Kind
      </h6>
      <div class="flex flex-wrap">
        <div class="w-full lg:w-6/12 px-4">
          <div class="relative w-full mb-3">
            <label class="block text-xs font-semibold mb-2" for="grid-username">
              Name, Vorname
            </label>
            <input
              id="grid-username"
              type="text"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
        <div class="w-full lg:w-6/12 px-4">
          <div class="relative w-full mb-3">
            <label class="block text-xs font-semibold mb-2" for="grid-email">
              Geburtsdatum
            </label>
            <input
              id="grid-email"
              type="date"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
        <div class="w-full lg:w-6/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block text-xs font-semibold mb-2"
              for="grid-first-name"
            >
              Herkunft (bei mehreren bitte alle angeben. Wird ausschliesslich zu
              statistischen Zwecken verwendet)
            </label>
            <input
              id="grid-first-name"
              type="text"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
        <div class="w-full lg:w-6/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block text-xs font-semibold mb-2"
              for="grid-last-name"
            >
              Motivationsgrund für die Anmeldung sowie allfällige
              tänzerische/sportliche Erfahrung
            </label>
            <textarea
              id="grid-about-me"
              type="text"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
              rows="4"
            />
          </div>
        </div>
      </div>

      <hr class="mt-6 border-b-1 border-blueGray-300" />
      <br />

      <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
        Erziehungsberechtigte
      </h6>
      <div class="flex flex-wrap">
        <div class="w-full lg:w-12/12 px-4">
          <div class="relative w-full mb-3">
            <label class="block text-xs font-semibold mb-2" for="grid-address">
              Name, Vorname
            </label>
            <input
              id="grid-address"
              type="text"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
        <div class="w-full lg:w-4/12 px-4">
          <div class="relative w-full mb-3">
            <label class="block text-xs font-semibold mb-2" for="grid-city">
              Strasse, Nr, PLZ, Ort
            </label>
            <input
              id="grid-city"
              type="email"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
        <div class="w-full lg:w-4/12 px-4">
          <div class="relative w-full mb-3">
            <label class="block text-xs font-semibold mb-2" for="grid-country">
              E-mail
            </label>
            <input
              id="grid-country"
              type="email"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
        <div class="w-full lg:w-4/12 px-4">
          <div class="relative w-full mb-3">
            <label
              class="block text-xs font-semibold mb-2"
              for="grid-postal-code"
            >
              Telefonnr.
            </label>
            <input
              id="grid-postal-code"
              type="tel"
              class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
            />
          </div>
        </div>
      </div>
    </form>
  </div>
</div>
