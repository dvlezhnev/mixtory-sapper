<script>
    export let story;
    export let posterColor = "#" + ("0".repeat(5) + Math.random() * (0xFFFFFF + 1)).slice(-6);
</script>

<a class="story-container" href="/stories/{story.slug}">
    <div class="poster" style="background-color: {posterColor};"></div>
    <div class="title">{story.title}</div>
</a>

<style>
    .story-container{
        display: block;
        width: 250px;
        height: 260px;
        background-color: #FFFFFF;
        overflow: hidden;
        box-shadow: 4px 4px 10px rgba(2, 13, 33, 0.08);
        border-radius: 4px;
        margin-top: 48px;
        margin-right: calc(160px / 3);
        text-decoration: none;
    }
    .story-container:nth-child(4n){
        margin-right: 0;
    }

    .story-container:hover{
        box-shadow: 4px 4px 10px rgba(2, 13, 50, 0.3);
    }
    a.story-container:focus{
        box-shadow: 4px 4px 10px rgba(2, 13, 50, 0.3);
        outline: none;
    }


    .story-container > .poster{
        background-color: #E8E8E8;
        width: 100%;
        height: 160px;
    }

    .story-container > .title{
        width: 100%;
        box-sizing: border-box;
        padding: 20px 20px 0 20px;
        font-style: normal;
        font-weight: 600;
        font-size: 18px;
        line-height: 23px;
        color: #120D24;
    }
</style>