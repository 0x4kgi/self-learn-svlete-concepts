<script>
    let count = 0;

    function incrementCounter() {
        count += 1;
    }
</script>

<button on:click={incrementCounter}>
    The count is: {count}
</button>
