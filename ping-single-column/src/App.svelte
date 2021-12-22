<script lang="ts">
    import Logo from "./components/Logo.svelte";
    import Title from "./components/Title.svelte";
</script>

<div id="app">
    <div id="container">
        <Logo />
        <Title />
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
