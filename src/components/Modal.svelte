<script>
  export let open = false
  export let close = () => {}
</script>

{#if open}
  <div
    class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50"
  >
    <div class="bg-white p-6 rounded-lg shadow-lg max-w-lg w-full relative">
      <button
        class="absolute top-2 right-2 text-gray-500 hover:text-gray-700"
        on:click={close}
      >
        &times;
      </button>
      <slot></slot>
    </div>
  </div>
{/if}
