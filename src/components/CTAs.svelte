<script>
  import BookModal from './BookModal.svelte'
  let showBookModal = false

  const handleClose = () => {
    showBookModal = false
  }
</script>

<div class="flex items-center gap-4">
  <button class={'specialBtnDark'} on:click={() => (showBookModal = true)}>
    <p class="text-base sm:text-lg md:text-xl">Buche eine Show</p>
  </button>
  <BookModal show={showBookModal} on:close={handleClose} />

  <a href="/register">
    <button class="specialBtn">
      <p class="text-base sm:text-lg md:text-xl">Komm tanz mit uns</p>
    </button>
  </a>
</div>
