<script>
    import { count } from "./store";

    function upd() {
        count.update((n) => n - 1);
    }
</script>

<button on:click={upd}>-</button>
