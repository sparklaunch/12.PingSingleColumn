<script lang="ts">
    import Logo from "./components/Logo.svelte";
    import Title from "./components/Title.svelte";
    import Form from "./components/Form.svelte";
    import Dashboard from "./components/Dashboard.svelte";
    import Shares from "./components/Shares.svelte";
    import Footer from "./components/Footer.svelte";
</script>

<div id="app">
    <div id="container">
        <Logo />
        <Title />
        <Form />
        <Dashboard />
        <Shares />
        <Footer />
    </div>
</div>

<style>
    #app {
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    #container {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    @media all and (max-width: 1440px) {
        #app {
            display: block;
            height: auto;
            padding: 100px 0;
        }
        #container {
            width: 90%;
            margin: auto;
            align-items: stretch;
        }
    }
</style>
