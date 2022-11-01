<div class="box">
    {#if $$slots.heading}
        <h3>
            <slot name="heading">
                <span class="missing">Unnamned Box</span>
            </slot>
        </h3>
    {/if}
    <slot />
</div>

<style>
    .box {
        width: 50vw;
        margin: auto;
        margin-top: 0.5em;
        border: 1px solid gray;
        border-radius: 0.5em;
        padding: 0.5em;
    }

    h3 {
        font-style: italic;
    }
</style>
