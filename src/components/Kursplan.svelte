<script>
  import KursplanModal from './KursplanModal.svelte'
  let showKursplanModal = false

  const handleKursplanClose = () => {
    showKursplanModal = false
  }
</script>

<div class="flex items-center gap-4">
  <button class="specialBtn" on:click={() => (showKursplanModal = true)}>
    <p class="text-base sm:text-lg md:text-xl">Buche eine Show</p>
  </button>
  <KursplanModal show={showKursplanModal} on:close={handleKursplanClose} />
</div>
