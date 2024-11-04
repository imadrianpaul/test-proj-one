<!-- src/App.svelte -->
<script>
  import LoginOverlay from '../pages/Login/LoginOverlay.svelte';
  let showLogin = false;
</script>

<button on:click={() => showLogin = true}>Login</button>
<LoginOverlay isVisible={showLogin} />
