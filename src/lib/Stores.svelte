<script>
    import Decrement from "./Stores/Decrement.svelte";
    import Increment from "./Stores/Increment.svelte";
    import Custom from "./Stores/Custom.svelte";
    import { count } from "./Stores/store";

    let countValue;

    const unsubscribe = count.subscribe((value) => (countValue = value));
</script>

The count is {countValue}

<Increment />
<Decrement />
<Custom />
