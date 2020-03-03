<script>
    export let story;
    export let posterColor = "#" + ("0".repeat(5) + Math.random() * (0xFFFFFF + 1)).slice(-6);

    let href = `/stories/${story.slug}`;
</script>

<a class="story-container" href="{href}">
    <div class="poster" style="background-color: {posterColor};">
        {#if story.adult === true}
        <div class="adult-alert">
            <div class="age"><span>18+</span></div>
            <div class="text"><span>содержит нецензурную брань</span></div>
        </div>
        {/if}
    </div>
    <div class="title">{story.title}</div>
</a>

<style type="text/scss">
    .story-container{
        flex-grow: 1;
        flex-basis: 250px;
        display: block;
        height: 260px;
        background-color: #FFFFFF;
        overflow: hidden;
        box-shadow: 4px 4px 10px rgba(2, 13, 33, 0.08);
        border-radius: 4px;
        margin: 24px 20px;
        text-decoration: none;

        &:hover{
            box-shadow: 4px 4px 10px rgba(2, 13, 50, 0.3);
        }

        &:focus{
            box-shadow: 4px 4px 10px rgba(2, 13, 50, 0.3);
            outline: none;
        }
    }

    .poster{
        background-color: #E8E8E8;
        width: 100%;
        height: 160px;
        position: relative;

        & > .adult-alert
        {
            width: 100%;
            position: absolute;
            bottom: 0;
            left: 0;
            display: flex;
            align-content: center;
            align-items: center;
            height: 32px;

            & > .age{
                & > span{
                    font-family: 'Montserrat', sans-serif;
                    font-style: normal;
                    font-weight: 600;
                    font-size: 18px;
                    line-height: 22px;
                    color: #ffffff;
                    align-self: center;
                }
                height: 100%;
                background-color: rgba(255,255,255,.5);
                display: inline-flex;
                align-content: center;
                justify-content: center;
                padding: 0 8px;
            }

            & > .text{
                & > span{
                    font-family: 'Montserrat', sans-serif;
                    font-style: normal;
                    font-weight: 500;
                    font-size: 12px;
                    line-height: 16px;
                    color: #ffffff;
                    align-self: center;
                }
                height: 100%;
                background-color: rgba(255,255,255,.2);
                flex-grow: 1;
                display: inline-flex;
                align-content: center;
                justify-content: flex-start;
                padding-left: 8px;
            }
        }
    }

    .title{
        width: 100%;
        box-sizing: border-box;
        padding: 20px 20px 0 20px;
        font-style: normal;
        font-weight: 600;
        font-size: 18px;
        line-height: 23px;
        color: #120D24;
    }

    @media (max-width: 600px){
        .story-container{
            height: auto;
        }
        .title{
            padding: 12px;
        }
    }
</style>
