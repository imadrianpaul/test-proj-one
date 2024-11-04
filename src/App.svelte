<script>
  import LoginOverlay from "./pages/Login/LoginOverlay.svelte";
  let showLogin = false;
</script>

{#if !showLogin}
  
<button on:click={() => showLogin = true}>Login</button>

{/if}
<LoginOverlay isVisible={showLogin} />


