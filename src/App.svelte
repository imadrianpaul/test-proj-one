<script>

  import Navbar from "./components/Navbar.svelte";
  import MainLayout from "./layouts/MainLayout.svelte";
  import LoginOverlay from "./pages/Login/LoginOverlay.svelte";
  import Home from "./pages/Home/Home.svelte";

  let showLogin = false;

  function toggleLogin() {
    showLogin = !showLogin;
  }

</script>

<MainLayout>
  <Navbar on:toggleLogin={toggleLogin} />
  <Home />
</MainLayout>

<LoginOverlay isVisible={showLogin} />

<style>
</style>


