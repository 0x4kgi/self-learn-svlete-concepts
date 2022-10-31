<script>
    import { count } from "./store";

    let value;

    function updateCustomValue() {
        count.update((n) => (n = value));
    }
</script>

<input type="text" bind:value />
<button on:click={updateCustomValue}>update</button>
