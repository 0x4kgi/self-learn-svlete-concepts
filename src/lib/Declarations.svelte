<script>
    let count = 0;

    function incrementCounter() {
        count += 1;
    }

    $: doubled = count * 2;
    $: quad = count * 4;
</script>

<button on:click={incrementCounter}>
    The count is: {count}
</button>
<p>Doubled: {doubled}</p>
<p>Quad: {quad}</p>
