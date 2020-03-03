<script>
    import StoryListElement from "./StoryListElement.svelte";
    export let title = "Название блока";
    export let stories = [];
</script>

<div class="wrapper">
    <div class="container">
        <h2>{title}</h2>
        <div class="elements">
            {#each stories as story}
                <StoryListElement story="{story}" posterColor="{story.backColor}"/>
            {/each}
        </div>
    </div>
</div>

<style>
    .wrapper{
        width: 100%;
        background-color: #ffffff;
    }
    .container{
        margin: auto;
        max-width: 1400px;
        padding: 88px 120px 64px 120px;
        box-sizing: border-box;
        overflow: hidden;
    }

    .elements{
        width: calc(100% + 40px);
        margin-left: -20px;
        margin-right: -20px;
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

    @media (max-width: 1024px){
        .container{
            padding: 24px 12px 12px 12px;
        }
    }
</style>
