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
        <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
          <h6
            class="text-4xl sm:text-5xl md:text-4xl max-w-[1000px] mx-auto w-full font-semibold text-center text-red-500 pt-6"
          >
            Kursplan & Preise
          </h6>

          <!-- Table content -->
          <div class="overflow-x-auto mt-8">
            <table class="w-full border-collapse">
              <thead>
                <tr class="bg-gray-200">
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2">Woche 1 bis 3</th>
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2"></th>
                </tr>
              </thead>
              <tbody>
                <tr class="bg-gray-100">
                  <th class="border px-4 py-2"></th>
                  <td class="border px-4 py-2">10:30 - 11:30</td>
                  <td class="border px-4 py-2">11:30 - 12:30</td>
                  <td class="border px-4 py-2">12:30 - 13:10</td>
                  <td class="border px-4 py-2">13:10 - 14:00</td>
                </tr>
                <!-- TEENIES -->
                <tr>
                  <th class="border px-4 py-2">Teenies</th>
                  <td class="border px-4 py-2"
                    >Traditioneller Tanz <br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-4 py-2"
                    >Afro Beats<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle Freies Gymi
                  </td>
                  <td class="border px-4 py-2"></td>
                  <td class="border px-4 py-2">Gesang</td>
                </tr>
                <!-- MINI F -->
                <tr>
                  <th class="border px-4 py-2">Mini F</th>
                  <td class="border px-4 py-2"
                    >Afro Beats<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-4 py-2"
                    >Traditioneller Tanz<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-4 py-2"></td>
                  <td class="border px-4 py-2">Gesang</td>
                </tr>
                <!-- MINI A -->
                <tr>
                  <th class="border px-4 py-2">Mini A</th>
                  <td class="border px-4 py-2"
                    >Traditioneller Tanz<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-4 py-2"
                    >Afro Beats<br />
                    <i class="fa-solid fa-location-dot"></i>
                    Turnhalle GZ Riesbach
                  </td>
                  <td class="border px-4 py-2"></td>
                  <td class="border px-4 py-2">Gesang</td>
                </tr>
              </tbody>
            </table>
          </div>

          <!-- Table 2 content -->
          <div class="overflow-x-auto mt-8">
            <table class="w-full border-collapse">
              <thead>
                <tr class="bg-gray-200">
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2">Woche 1 bis 3</th>
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2"></th>
                </tr>
              </thead>
              <tbody>
                <tr class="bg-gray-100">
                  <th class="border px-4 py-2"></th>
                  <td class="border px-4 py-2">10:30 - 11:30</td>
                  <td class="border px-4 py-2">11:30 - 12:30</td>
                  <td class="border px-4 py-2">12:30 - 13:10</td>
                  <td class="border px-4 py-2">13:10 - 14:00</td>
                </tr>
                <tr>
                  <th class="border px-4 py-2">Teenies</th>
                  <td class="border px-4 py-2">Traditioneller Tanz</td>
                  <td class="border px-4 py-2">Afro Beats</td>
                  <td class="border px-4 py-2"></td>
                  <td class="border px-4 py-2">Gesang</td>
                </tr>
                <tr>
                  <th class="border px-4 py-2">Teenies</th>
                  <td class="border px-4 py-2">Traditioneller Tanz</td>
                  <td class="border px-4 py-2">Afro Beats</td>
                  <td class="border px-4 py-2"></td>
                  <td class="border px-4 py-2">Gesang</td>
                </tr>
                <tr>
                  <th class="border px-4 py-2">Teenies</th>
                  <td class="border px-4 py-2">Traditioneller Tanz</td>
                  <td class="border px-4 py-2">Afro Beats</td>
                  <td class="border px-4 py-2"></td>
                  <td class="border px-4 py-2">Gesang</td>
                </tr>
              </tbody>
            </table>
          </div>

          <!-- buttons -->
          <div class="flex items-center gap-4 justify-center pt-10">
            <button class="specialBtnDark">
              <p class="text-base sm:text-lg md:text-xl">Close</p>
            </button>
          </div>
        </div>
      </div>
    </SectionWrapper>
  </div>
{/if}
