
<script>
    import LoginOverlay from './pages/Login/LoginOverlay.svelte';
    let showLogin = false;

    function toggleLogin() {
        showLogin = !showLogin;
    }
</script>

<div class="home-container">
    <div>
        <h1>uParcel</h1>
        <p>Your easiest way to deliver</p>
        <button on:click={toggleLogin}>Login</button>
    </div>
</div>


<LoginOverlay isVisible={showLogin} />

<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    .home-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-image: url('../assets/pexels-gaho-chen-2766129-10583179.jpg');
        background-size: cover;
        background-position: center;
        color: black;
        text-align: center;
        font-family: 'Poppins', sans-serif;
    }

    h1 {
        font-size: 2.5rem;
    }

    p {
        font-size: 1.2rem;
    }

    button {
        margin-top: 1rem;
        padding: 0.5rem 1rem;
        font-size: 1rem;
        cursor: pointer;
        border: none;
        border-radius: 5px;
        background-color: #007bff;
        color: white;
    }
</style>
