<script>
    import StoryTitle from "./StoryTitle.svelte";
    import StoryClause from "./StoryClause.svelte";

    export let story;

    let title = story.title;
    let clauses = [];

    let currentIndex = -1;
    let clause = "";
    let finished = false;

    function mixClauses() {
        clauses = story.clauses
                .slice()
                .map(c => {
                    return {
                        order: Math.random(),
                        clause: c
                    }
                })
                .sort((a, b) => a.order - b.order);
    }

    function next() {
        let nextIndex = currentIndex + 1;
        if (nextIndex < clauses.length)
        {
            clause = clauses[nextIndex].clause;
            currentIndex = nextIndex;
        }
        if (nextIndex === clauses.length - 1)
        {
            finished = true;
        }
    }

    function onStartButtonClick() {
        mixClauses();
        next();
    }
</script>

<div class="wrap" style="background: linear-gradient(180deg, rgba(2,0,36,1) 0%, rgba(18,13,36,1) 300px, rgba(255,255,255,1) 300px, rgba(255,255,255,1) 100%);">
    <div class="container">
        {#if currentIndex === -1}
            <StoryTitle title="{title}"/>
        {:else}
            <StoryClause clause="{clause}"/>
        {/if}
        <div class="controls">
            {#if currentIndex === -1}
                <button on:click={onStartButtonClick}>Перемешать</button>
            {:else}
                <button on:click={next}>Следующая →</button>
            {/if}
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
    }
    .controls{
        padding-top: 68px;
        text-align: center;
    }
    .controls > button{
        padding: 24px;
        font-weight: 600;
        font-size: 16px;
        line-height: 18px;
        color: #FFFFFF;
        background: #22C06B;
        border-radius: 4px;
        border: none;
    }
</style>