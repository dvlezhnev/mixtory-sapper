<script>
    import StoryTitle from "./StoryTitle.svelte";
    import StoryClause from "./StoryClause.svelte";
    import {factorial} from "../../utils/Math";
    import StoryBackgroud from "./StoryBackdrop.svelte";
    import StoryBackdrop from "./StoryBackdrop.svelte";

    export let story;

    let title = story.title;
    let titleBackColor = story.titleBackColor;
    let clauses = [];

    let currentIndex = -1;
    let clause = "";
    let finished = false;
    let countVariant = factorial(story.clauses.length).toLocaleString('ru-RU');

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
        if (nextIndex < clauses.length) {
            clause = clauses[nextIndex].clause;
            currentIndex = nextIndex;
        }
        if (nextIndex === clauses.length - 1) {
            finished = true;
        }
    }

    function onStartButtonClick() {
        finished = false;
        currentIndex = -1;
        mixClauses();
        next();
    }
</script>

<svelte:head>
    <meta name="theme-color" content="{story.backdropColor}">
    <meta name="apple-mobile-web-app-status-bar-style" content="{story.backdropColor}">
    <meta property="og:locale" content="ru_RU"/>
    <meta property="og:type" content="article"/>
    <meta property="og:title" content="{story.title}"/>
    <meta name="description" content="Делюсь 1 из возможных {countVariant} вариантов развития истории. Замиксуйте свою версию!"/>
    <meta property="og:description" content="Делюсь 1 из возможных {countVariant} вариантов развития истории. Замиксуйте свою версию!"/>
    <meta property="og:image" content="https://mixtory.ru/assets/share_covers/{story.shareCover}"/>
    <meta property="og:image:width" content="751"/>
    <meta property="og:image:height" content="392"/>
    <meta property="vk:image" content="https://mixtory.ru/assets/share_covers/{story.shareCover}"/>
    <meta property="og:url" content="https://mixtory.ru/stories/{story.slug}"/>
    <meta property="og:site_name" content="Mixtory"/>
</svelte:head>

<div class="wrapper">
    <StoryBackdrop {story}/>
    <div class="container">
        {#if currentIndex === -1}
            <StoryTitle title="{title}" {titleBackColor}/>
        {:else}
            <StoryClause clause="{clause}"/>
        {/if}
        <div class="controls">
            {#if finished}
            <div class="info">
                <span>Вы только что прочитали</span>
                <span class="big">1</span>
                <span>из возможных</span>
                <span class="big">{countVariant}</span>
                <span>вариантов развития истории</span>
            </div>
            <div class="finished-buttons-container">
                <button on:click={onStartButtonClick}>Перемешать заново</button>
                <a href=".">Выбрать другую историю →</a>
            </div>
            {/if}
            {#if currentIndex === -1}
                <button on:click={onStartButtonClick}>Перемешать</button>
            {:else if finished === false}
                <button on:click={next}>Следующая →</button>
            {/if}
        </div>
    </div>
</div>

<style type="text/scss">
    .wrapper{
        width: 100%;
        position: relative;
    }
    .container{
        margin: auto;
        max-width: 1400px;
        padding: 88px 120px 64px 120px;
        box-sizing: border-box;
    }
    
    @media (max-width: 1024px) {
        .container{
            padding: 12px;
        }
    }
    .controls{
        padding-top: 68px;
        text-align: center;
    }
    .controls  button{
        padding: 20px;
        font-weight: 600;
        font-size: 16px;
        line-height: 18px;
        color: #FFFFFF;
        background: #22C06B;
        border-radius: 4px;
        border: 4px solid #22C06B;
        cursor: pointer;
    }

    .controls > .info{
        /*margin-top: 88px;*/
        box-sizing: border-box;
        display: flex;
        align-items: center;
        justify-content: space-between;

        @media (max-width: 1024px) {
            & {
                flex-direction: column;
            }
        }
    }

    .controls > .info > span{
        font-family: Merriweather, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 15px;
        line-height: 19px;
        color: #120D24;
    }

    .controls > .info > span.big{
        font-family: Montserrat, sans-serif;
        font-weight: 500;
        font-size: 38px;
        line-height: 53px;
        color: #120D24;

        @media (max-width: 1024px) {
            & {
                font-size: 28px;
            }
        }
    }

    .controls > .finished-buttons-container{
        padding-top: 64px;
        display: flex;
        justify-content: flex-end;

        @media (max-width: 1024px) {
            & {
                flex-direction: column;
            }
        }
    }

    .controls > .finished-buttons-container > button{
        background-color: #ffffff;
        color: #120D24;
    }

    .controls > .finished-buttons-container > a{
        display: inline-block;
        padding: 20px;
        font-weight: 600;
        font-size: 16px;
        line-height: 18px;
        color: #FFFFFF;
        background: #22C06B;
        border-radius: 4px;
        border: 4px solid #22C06B;
        cursor: pointer;
        text-decoration: none;
        margin-left: 32px;

        @media (max-width: 1024px) {
            & {
                flex-direction: column;
                margin-left: 0;
                margin-top: 1rem;
            }
        }
    }
</style>
