<script>

    import LoginOverlay from '../pages/Login/LoginOverlay.svelte';
    
 
    let showLogin = false;
    export let toggleLogin;

</script>

<div class="main-layout">
    <header>

        
    </header>

    <main>



        <slot />
    </main>

    <footer>

    </footer>

    {#if showLogin}
        <LoginOverlay isVisible={showLogin} />
    {/if}

</div>

<style>

</style>