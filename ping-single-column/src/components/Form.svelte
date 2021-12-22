<script lang="ts">
    import { slide } from "svelte/transition";
    let email: string;
    let emptyEmailWarning,
        invalidEmailWarning: boolean = false;
    const emailRegex: RegExp = new RegExp(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
    );
    const submitHandler: () => void = () => {
        if (!email) {
            emptyEmailWarning = true;
        } else if (!email.match(emailRegex)) {
            emptyEmailWarning = false;
            invalidEmailWarning = true;
        } else {
            emptyEmailWarning = false;
            invalidEmailWarning = false;
        }
    };
</script>

<div id="form">
    <form on:submit|preventDefault={submitHandler} novalidate>
        <input
            type="email"
            name="email"
            bind:value={email}
            class:warning={emptyEmailWarning || invalidEmailWarning}
            placeholder="Your email address..."
            required
        />
        {#if emptyEmailWarning}
            <p transition:slide>Email cannot be empty</p>
        {:else if invalidEmailWarning}
            <p transition:slide>Please provide a valid email address</p>
        {/if}
        <input type="submit" value="Notify Me" />
    </form>
</div>

<style>
    #form > form {
        position: relative;
    }
    #form > form > p {
        position: absolute;
        top: 55px;
        left: 25px;
        color: rgb(204, 133, 141);
        font-style: italic;
        font-size: 12px;
    }
    input::placeholder {
        color: rgb(200, 206, 217);
    }
    #form {
        margin-bottom: 80px;
    }
    input[type="email"] {
        border: 1px solid rgb(222, 227, 249);
        padding: 15px 25px;
        border-radius: 30px;
        margin-right: 10px;
        width: 400px;
        transition: border 0.3s;
    }
    input[type="submit"] {
        border: none;
        padding: 15px 50px;
        color: white;
        background-color: rgb(67, 112, 242);
        border-radius: 30px;
        font-weight: 600;
        box-shadow: 5px 5px 5px rgba(67, 112, 242, 0.25);
        cursor: pointer;
        transition: filter 0.3s;
    }
    input[type="submit"]:hover {
        filter: brightness(0.9);
    }
    input[type="submit"]:active {
        filter: brightness(1.1);
    }
    .warning {
        border: 1px solid rgb(204, 133, 141) !important;
    }
</style>
