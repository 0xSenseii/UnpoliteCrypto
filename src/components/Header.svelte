<script>
    export let connected;
</script>

<main>
    <h1>💣 Unpolite Crypto 💣</h1>

    {#if connected === false}
        <div class="dot">🔴 Not connected</div>
    {/if}

    {#if connected === true}
        <div class="dot">🟢 Connected</div>
    {/if}
</main>

<style>
    /* place dot to the right of the h1 */
    .dot {
        position: absolute;
        right: 5%;
        top: 5%;
        font-size: 1.3em;
        color: #ffd900;
    }
</style>
