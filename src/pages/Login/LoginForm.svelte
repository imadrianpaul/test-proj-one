<script>
    export let close;

    function handleSubmit(event) {
        event.preventDefault();
        close(); // Close overlay after submission
    }
</script>

<div class="login-box">
    <h2>LOGIN AS CUSTOMER</h2>
    <h3>Enter the following to Log-in to uParcel</h3>
    <div class="separator"></div>

    <div class="content-form" on:submit|preventDefault={handleSubmit}>
        <div class="email">
            <label for="emailadd"></label>
            <input type="text" id="emailadd" placeholder="Email address" required />
        </div>
        <div class="pword">
            <label for="password"></label>
            <input type="password" id="password" placeholder="Password" required />
        </div>
        <button class="button-1" type="submit">Login Now</button>
        <h3> 
            <a href="/forgotpassword" class="forgot-pass">Forgot Password?</a>
        </h3>
        <h3> Don't have an account?
            <a href="/register" class="register-link">Register</a>
            now.
        </h3>
    </div>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    .overlay {
        display: flex;
        align-items: center;
        justify-content: center;
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        background-color: rgba(198, 198, 198, 0.5);
    }



    .login-box {
        background-color: white;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        padding: 2rem;
        text-align: center;
        max-width: 500px;
        width: 100%;
    }

    .content-form {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .separator {
        width: 100%;
        height: 1px;
        background-color: #f5ab35;
        margin: 1rem 0;
    }

    .email, .pword {
        font-family: "Poppins", sans-serif, serif;
        padding: 1rem; /* Increase padding for larger input fields */
        border: 1px solid var(--border-color);
        border-radius: 10px;
        max-width: 400px;
        width: 100%;
        font-size: 1rem;
    }



    .email input,
    .pword input,
    .button-1 {
        padding: 10px 20px;
        border: 1px solid;
        border-color: #e7e8ec;
        border-radius: 3px;
        height: 55px;
        width: 100%;
        font-size: 14px;
        font-weight: 300;
        text-transform: none;
        box-sizing: border-box;
}

    .button-1 {
        background-color: #f5ab35;
        font-weight: 900;
        letter-spacing: 1px;
        width: 100%;
        height: 55px;
        color: #fff;
        text-transform: uppercase;
        display: flex;
        align-items: center;
        justify-content: center;

    }

    .forgot-pass {
        color: rgb(135, 135, 135);
    }

    .forgot-pass:hover {
        color: #f5ab35;
        transition: 0.5s ease;
    }

    .register-link {
        color: #f5ab35;
        text-decoration: underline;
    }

    .register-link:hover {
        text-decoration: none;
    }

    .email input:focus,
    .pword input:focus {
        border-color: #f5ab35;
        outline: none;

    }

    .button-1:hover {
        background-color: rgb(32, 32, 32);
        transition: 0.5s ease;
    }

</style>
