<script>
  import BookModal from './BookModal.svelte'
  let showBookModal = false

  const handleBookClose = () => {
    showBookModal = false
  }
</script>

<div class="flex items-center gap-4">
  <button class="specialBtn" on:click={() => (showBookModal = true)}>
    <p class="text-base sm:text-lg md:text-xl">Buche eine Show</p>
  </button>
  <BookModal show={showBookModal} on:close={handleBookClose} />
</div>
