<script>
    import HelloWorld from "./lib/HelloWorld.svelte";
    import Counter from "./lib/Counter.svelte";
    import Declarations from "./lib/Declarations.svelte";
    import Props from "./lib/Props.svelte";
    import Stores from "./lib/Stores.svelte";
    import Box from "./lib/layout/Box.svelte";
</script>

<main>
    <Box>
        <HelloWorld />
    </Box>

    <Box>
        <span slot="heading">Counter box</span>
        <Counter />
    </Box>

    <Box>
        <span slot="heading">$: thingies</span>
        <Declarations />
    </Box>

    <Box>
        <span slot="heading">Props to components</span>
        <p><Props passedValue="hello" /></p>
        <p><Props passedValue="1" /></p>
        <p><Props passedValue="3" /></p>
        <p><Props passedValue={{ name: "value" }} /></p>
    </Box>

    <Box>
        <span slot="heading">"Global variables"</span>
        <Stores />
    </Box>
</main>

<style>
</style>
