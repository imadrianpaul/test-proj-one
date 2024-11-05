<script>
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher();

    function handleLoginClick() {
        dispatch("toggleLogin");
    }
</script>

<div class="navbar-row top-row">
    <div class="left-section">
        <a href="/track">Track Delivery</a>
        <a href="/request">Request Delivery</a>
        <a href="/languages">Languages</a>
    </div>
    <div class="right-section">
        <a href="/signup">Sign Up</a>
        <button on:click={handleLoginClick}>Login</button>
    </div>
</div>

<div class="navbar-row bottom-row">
    <div class="nav-bar-logo">
        <a href="/">uParcel</a>
    </div>
    <div class="menu">
        <a href="/services">Services</a>
        <a href="/how-it-works">How It Works?</a>
        <a href="/tracking">Tracking</a>
        <a href="/faqs">FAQs</a>
        <a href="/rates">Rates</a>
        <a href="/rates">Contact Us</a>
        <a href="/rates">Agent</a>
        <a href="/rates">Blog</a>
    </div>
</div>

<style>

    .navbar-row {
        display: flex;
        align-items: center;
        padding: 0.5rem 2rem;
        background-color: #f8f9fa;
    }

    .top-row {
        justify-content: space-between;
        font-size: 0.9rem;
        border-bottom: 1px solid #ddd;
    }

    .bottom-row {
        justify-content: space-between;
        font-size: 1rem;
        background-color: #fff;
    }

    .left-section, .right-section, .menu {
        display: flex;
        gap: 1.5rem;
    }


    .nav-bar-logo h1 {
        font-size: 1.5rem;
        margin: 0;
    }


    a, button {
        color: #333;
        text-decoration: none;
        font-weight: 500;
    }

    button {
        background: none;
        border: none;
        cursor: pointer;
        color: #007bff;
    }

    button:hover, a:hover {
        color: #0056b3;
    }

</style>