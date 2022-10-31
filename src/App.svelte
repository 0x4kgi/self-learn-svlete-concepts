<script>
    import HelloWorld from "./lib/HelloWorld.svelte";
    import Counter from "./lib/Counter.svelte";
    import Declarations from "./lib/Declarations.svelte";
</script>

<main>
    <HelloWorld />

    <p><Counter /></p>

    <p><Declarations /></p>

    <p />
</main>

<style>
    main {
        text-align: center;
        margin: auto;
        font-size: larger;
    }
</style>
