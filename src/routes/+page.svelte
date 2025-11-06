<script>
  import { onMount } from 'svelte'
  import Intro from '../components/Intro.svelte'
  import Kurse from '../components/Kurse.svelte'
  import Shows from '../components/Shows.svelte'
  import Footer from '../components/Footer.svelte'
  import PopupModal from '../components/PopupModal.svelte'
  import UnserTeam from '../components/UnserTeam.svelte'

  let showPopupModal = false

  onMount(() => {
    showPopupModal = true // open modal once page loads
  })

  const handlePopupClose = () => {
    showPopupModal = false
  }
</script>

{#if showPopupModal}
  <PopupModal show={showPopupModal} on:close={handlePopupClose} />
{/if}

<main class="flex flex-col">
  <Intro />
  <Kurse />
  <Shows />
  <UnserTeam />
  <Footer />
</main>
