<!-- loginform.svelte -->
<script>
    export let close;

    function handleSubmit(event) {
        event.preventDefault();
        close(); // Close overlay after submission
    }
</script>

<style src="./Login.css"></style>

<div class="login-box">
    <h2>Login as customer</h2>
    <form on:submit|preventDefault={handleSubmit}>
        <div class="uname">
            <label for="username">Username</label>
            <input type="text" id="username" required />
        </div>
        <div class="pword">
            <label for="password">Password</label>
            <input type="password" id="password" required />
        </div>
        <button type="submit">Login</button>
    </form>
</div>
