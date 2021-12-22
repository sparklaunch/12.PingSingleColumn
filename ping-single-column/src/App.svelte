<script lang="ts">
    import Logo from "./components/Logo.svelte";
    import Title from "./components/Title.svelte";
    import Form from "./components/Form.svelte";
    import Dashboard from "./components/Dashboard.svelte";
    import Shares from "./components/Shares.svelte";
</script>

<div id="app">
    <div id="container">
        <Logo />
        <Title />
        <Form />
        <Dashboard />
        <Shares />
    </div>
</div>

<style>
    #app {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    #container {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>
