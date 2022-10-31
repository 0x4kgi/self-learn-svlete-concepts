<script>
    import HelloWorld from "./lib/HelloWorld.svelte";
    import Counter from "./lib/Counter.svelte";
    import Declarations from "./lib/Declarations.svelte";
    import Props from "./lib/Props.svelte";
    import Stores from "./lib/Stores.svelte";
</script>

<main>
    <HelloWorld />
    <hr />

    <p><Counter /></p>
    <hr />

    <p><Declarations /></p>
    <hr />

    <p><Props passedValue="hello" /></p>
    <p><Props passedValue="1" /></p>
    <p><Props passedValue="3" /></p>
    <p><Props passedValue={{ name: "value" }} /></p>
    <hr />

    <p><Stores /></p>
    <hr />
</main>

<style>
    main {
        text-align: center;
        margin: auto;
        font-size: larger;
    }
</style>
