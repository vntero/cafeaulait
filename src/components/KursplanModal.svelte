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
            Employee Information
          </h6>

          <!-- Table content -->
          <div class="overflow-x-auto mt-8">
            <table class="w-full border-collapse">
              <thead>
                <tr class="bg-gray-200 text-left">
                  <th class="px-4 py-2"></th>
                  <th class="px-4 py-2">Name</th>
                  <th class="px-4 py-2">Job</th>
                  <th class="px-4 py-2">Favorite Color</th>
                </tr>
              </thead>
              <tbody>
                <tr class="bg-gray-100">
                  <th class="border px-4 py-2">1</th>
                  <td class="border px-4 py-2">Cy Ganderton</td>
                  <td class="border px-4 py-2">Quality Control Specialist</td>
                  <td class="border px-4 py-2">Blue</td>
                </tr>
                <tr>
                  <th class="border px-4 py-2">2</th>
                  <td class="border px-4 py-2">Hart Hagerty</td>
                  <td class="border px-4 py-2">Desktop Support Technician</td>
                  <td class="border px-4 py-2">Purple</td>
                </tr>
                <tr class="bg-gray-100">
                  <th class="border px-4 py-2">3</th>
                  <td class="border px-4 py-2">Brice Swyre</td>
                  <td class="border px-4 py-2">Tax Accountant</td>
                  <td class="border px-4 py-2">Red</td>
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
