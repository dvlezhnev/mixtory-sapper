<script>
    export let clause = "";
    export let asHtml = false;
    console.log(clause);
</script>

<div class="container">
    <div class="clause">
        {#if asHtml}
            <h2>{@html clause}</h2>
        {:else}
            <h2>{clause}</h2>
        {/if}
    </div>
</div>

<style type="text/scss">
    .container{
        width: 100%;
        height: 100%;
        background-color: #FFFFFF;
        border-radius: 10px;
        padding: 10px;
        box-sizing: border-box;
        box-shadow: 4px 4px 10px rgba(2, 13, 33, 0.08);
    }
    .clause{
        margin: auto;
        width: 100%;
        text-align: center;
        border: 10px solid transparent;
        background-color: #FFFFFF;
        box-sizing: border-box;
        position: relative;
        /*padding: 140px 30px;*/
        min-height: 360px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    h2{
        font-family: 'Merriweather', serif;
        font-style: normal;
        font-weight: normal;
        font-size: 30px;
        line-height: 42px;
        color: #120D24;
        @media (max-width: 768px) {
            font-size: 22px;
            line-height: 30px;
        }
    }
</style>
