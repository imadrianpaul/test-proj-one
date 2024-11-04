<!-- src/lib/login/LoginOverlay.svelte -->
<script>
    import LoginForm from '../Login/LoginForm.svelte';
    export let isVisible = false;

    function close() {
        isVisible = false;
    }
</script>

{#if isVisible}
<div class="overlay">
    <LoginForm close={close} />
</div>
{/if}
