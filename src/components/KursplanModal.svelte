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
    class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50"
    on:click={close}
  >
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <SectionWrapper>
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-static-element-interactions -->
      <div
        class="relative flex flex-col w-full mb-6 shadow-lg rounded-lg max-w-[1000px] mx-auto m-20 bg-white max-h-screen overflow-y-auto"
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
          <h6
            class="text-xl sm:text-2xl md:text-3xl lg:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
          >
            Kursplan & Preise
          </h6>

          <!-- Table 1 content -->
          <div class="overflow-x-auto mt-8">
            <table
              class="w-full border-collapse text-xs sm:text-sm md:text-base lg:text-base"
            >
              <thead>
                <tr class="bg-gray-200">
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2">Samstag</th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                </tr>
              </thead>
              <!-- TEENIES -->
              <tbody>
                <tr class="bg-red-200">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2"></th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 10:30 - 11:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 11:30 - 12:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 12:30 - 13:10
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 13:10 - 14:00<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                </tr>
                <tr class="bg-red-200">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2">Teenies (ab 13)</th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >Traditioneller Tanz</td
                  >
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Afro Beats</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Pause</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Gesang</td>
                </tr>
                <!-- MINI F -->
                <tr class="bg-pink-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2"></th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 10:30 - 11:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 11:30 - 12:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 12:30 - 13:10
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 13:10 - 14:00<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                </tr>
                <tr class="bg-pink-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2">Mini F (Fortgeschritten ab 8)</th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Afro Beats</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >Traditioneller Tanz</td
                  >
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Pause</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Gesang</td>
                </tr>
                <!-- MINI A -->
                <tr class="bg-orange-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2"></th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 10:30 - 11:50<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 11:50 - 12:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 12:30 - 13:10
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 13:10 - 14:00<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                </tr>
                <tr class="bg-orange-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2">Mini A (Anfänger ab 6)</th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >Traditioneller Tanz</td
                  >
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Afro Beats</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Pause</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Gesang</td>
                </tr>
              </tbody>
            </table>
          </div>

          <!-- Last Saturday of the Month Table -->
          <div class="overflow-x-auto mt-8">
            <table
              class="w-full border-collapse text-xs sm:text-sm md:text-base lg:text-base"
            >
              <thead>
                <tr class="bg-gray-200">
                  <th class="px-2 sm:px-4 py-1 sm:py-2" colspan="5">
                    Letzter Samstag des Monats: ALLE zusammen
                  </th>
                </tr>
              </thead>
              <tbody>
                <tr class="bg-blue-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2"></th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 10:30 - 11:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 11:30 - 12:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 12:30 - 13:10
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 13:10 - 14:00<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                </tr>
                <tr class="bg-blue-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2">Alle</th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Gesang</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >CAL Stage Company</td
                  >
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Pause</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >CAL Stage Company</td
                  >
                </tr>
              </tbody>
            </table>
          </div>

          <!-- Preise Samstag Table Content -->
          <div class="overflow-x-auto mt-8">
            <table
              class="w-full border-collapse text-xs sm:text-sm md:text-base lg:text-lg"
            >
              <thead>
                <tr class="bg-green-300">
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2 text-center">
                    Preise Samstags: CHF 720 pro Semester (Geschwisterrabatt 50%)
                  </th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                </tr>
              </thead>
            </table>
          </div>

          <!-- Wednesday table -->
          <div class="overflow-x-auto mt-8">
            <table
              class="w-full border-collapse text-xs sm:text-sm md:text-base lg:text-base"
            >
              <thead>
                <tr class="bg-gray-200">
                  <th class="px-2 sm:px-4 py-1 sm:py-2" colspan="5">
                    Mittwochs

                  </th>
                </tr>
              </thead>
              <tbody>
                <tr class="bg-blue-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2"></th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 19:00 - 20:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Schulhaus Hofacker
                  <!-- </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"> -->
                    <!-- <i class="fa-solid fa-clock"></i> 11:30 - 12:30<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 12:30 - 13:10
                  </td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">
                    <i class="fa-solid fa-clock"></i> 13:10 - 14:00<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td> -->
                </tr>
                <tr class="bg-blue-100">
                  <th class="border px-2 sm:px-4 py-1 sm:py-2">Teenies (ab 12)</th>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Afrobeats Masterclass</td>
                  <!-- <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >CAL Stage Company</td -->
                  <!-- >
                  <td class="border px-2 sm:px-4 py-1 sm:py-2">Pause</td>
                  <td class="border px-2 sm:px-4 py-1 sm:py-2"
                    >CAL Stage Company</td -->
                  <!-- > -->
                </tr>
              </tbody>
            </table>
          </div>

          <!-- Preise Wednesday Table Content -->
          <div class="overflow-x-auto mt-8">
            <table
              class="w-full border-collapse text-xs sm:text-sm md:text-base lg:text-lg"
            >
              <thead>
                <tr class="bg-green-300">
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2 text-center">
                    Preise Mittwochs: CHF 30 pro Monat für Nichtmitglieder
                  </th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                  <th class="px-2 sm:px-4 py-1 sm:py-2"></th>
                </tr>
              </thead>
            </table>
          </div>

          <!-- Buttons -->
          <div class="flex items-center gap-4 justify-center pt-10">
            <button class="specialBtnCancel" on:click={close}>
              <p class="text-xs sm:text-sm md:text-base lg:text-lg">
                Schließen
              </p>
            </button>
          </div>

          
        </div>
      </div>
    </SectionWrapper>
  </div>
{/if}
