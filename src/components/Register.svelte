<script>
  import RegisterModal from './RegisterModal.svelte'
  let showRegisterModal = false

  const handleRegisterClose = () => {
    showRegisterModal = false
  }
</script>

<div class="flex items-center gap-4">
  <button
    class="specialBtnDark"
    on:click={() => {
      showRegisterModal = true
    }}
  >
    <p class="text-base sm:text-lg md:text-xl">Mach mit</p>
  </button>
  <RegisterModal
    show={showRegisterModal}
    on:close={() => {
      handleRegisterClose() // Close modal
    }}
  />
</div>
