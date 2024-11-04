<script>
    import LoginForm from "./LoginForm.svelte";
    export let isVisible = false;

    function close() {
        isVisible = false;
    }
</script>

<style src="./Login.css"></style>

{#if isVisible}
<div class="overlay">

        <LoginForm close={close} />

</div>
{/if}


