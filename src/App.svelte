<script>
    import HelloWorld from "./lib/HelloWorld.svelte";
    import Counter from "./lib/Counter.svelte";
    import Declarations from "./lib/Declarations.svelte";
    import Props from "./lib/Props.svelte";
    import Stores from "./lib/Stores.svelte";
    import Box from "./lib/layout/Box.svelte";

    let selectModule = "";

    let moduleList = [
        { target: "hello", text: "Hello world" },
        { target: "counter", text: "Counter" },
        { target: "declarations", text: "Declarations" },
        { target: "props", text: "Props" },
        { target: "global-vars", text: "global-vars" },
    ];

    function selectExample(prop) {
        selectModule = prop.target.value;
    }
</script>

<main>
    <Box>
        {#each moduleList as thing}
            <button on:click={selectExample} value={thing.target}>
                {thing.text}
            </button>
        {/each}
    </Box>

    {#if selectModule === "hello"}
        <Box>
            <HelloWorld />
        </Box>
    {:else if selectModule === "counter"}
        <Box>
            <span slot="heading">Counter box</span>
            <Counter />
        </Box>
    {:else if selectModule === "declarations"}
        <Box>
            <span slot="heading">$: thingies</span>
            <Declarations />
        </Box>
    {:else if selectModule === "props"}
        <Box>
            <span slot="heading">Props to components</span>
            <p><Props passedValue="hello" /></p>
            <p><Props passedValue="1" /></p>
            <p><Props passedValue="3" /></p>
            <p><Props passedValue={{ name: "value" }} /></p>
        </Box>
    {:else if selectModule === "global-vars"}
        <Box>
            <span slot="heading">"Global variables"</span>
            <Stores />
        </Box>
    {/if}
</main>

<style></style>
