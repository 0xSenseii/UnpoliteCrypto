<script>
    import Button from "./DownloadButton.svelte";
    export let src;
    export let href;
</script>

<div class="container__column">
    <!-- Cover -->
    <div class="content">
        <img src="./previews/{src}" alt="preview" />
        <Button href="./pdfs/{href}"/>
    </div>
</div>

<style>
    img {
        width: 50%;
        height: auto;
        border: 2px solid #ffd900;
        border-radius: 5px;
    }


    .container__column {
        /* center container column content */
        margin: 15px auto;
        display: flex;
        flex-basis: 33%;

        width: 50%;
        text-align: center;

        /* Layout each column */
        flex-direction: column;
    }

    .content {
        /* align content into the center */
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
