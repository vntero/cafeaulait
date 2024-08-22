<script>
  import BookModal from './BookModal.svelte'
  let showBookModal = false

  const handleBookClose = () => {
    showBookModal = false
  }

  import RegisterModal from './RegisterModal.svelte'
  let showRegisterModal = false

  const handleRegisterClose = () => {
    showRegisterModal = false
  }
</script>

<div class="flex items-center gap-4">
  <button class="specialBtnDark" on:click={() => (showBookModal = true)}>
    <p class="text-base sm:text-lg md:text-xl">Buche eine Show</p>
  </button>
  <BookModal show={showBookModal} on:close={handleBookClose} />

  <button class="specialBtn" on:click={() => (showRegisterModal = true)}>
    <p class="text-base sm:text-lg md:text-xl">Komm tanz mit uns</p>
  </button>
  <RegisterModal show={showRegisterModal} on:close={handleRegisterClose} />
</div>
