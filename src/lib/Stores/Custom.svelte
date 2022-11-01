<script>
    import { count } from "./store";

    let value;

    function updateCustomValue() {
        count.update((n) => (n = value));
    }
</script>

<input type="number" bind:value />
<button on:click={updateCustomValue}>update</button>
