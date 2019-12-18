<script>
    import StoryListElement from "./StoryListElement.svelte";
    export let title = "Название блока";
    export let stories = [];
</script>

<div class="wrap">
    <div class="container">
        <h2>{title}</h2>
        <div class="elements">
            {#each stories as story}
                <StoryListElement title="{story.title}"/>
            {/each}
        </div>
    </div>
</div>

<style>
    .wrap{

    }
    .container{
        margin: auto;
        width: 1400px;
        padding: 88px 120px 64px 120px;
        box-sizing: border-box;
        overflow: hidden;
    }

    .elements{
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
    }

    h2{
        font-style: normal;
        font-weight: 600;
        font-size: 32px;
        line-height: 46px;
        color: #120D24;
    }
</style>