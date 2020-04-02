<script>
    export let title;
    export let titleBackColor = "#DF7E7E";
</script>

<div class="container">
    <div class="title" style="background-color: {titleBackColor}">
        <h1>{title}</h1>
    </div>
</div>

<style>
    .container{
        width: 100%;
        height: 100%;
        background-color: #FFFFFF;
        border-radius: 10px;
        padding: 10px;
        box-sizing: border-box;
        box-shadow: 4px 4px 10px rgba(2, 13, 33, 0.08);
    }
    .title{
        margin: auto;
        width: 100%;
        text-align: center;
        border: 10px solid transparent;
        box-sizing: border-box;
        position: relative;
        padding: 140px 0;
        height: 360px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    h1{
        font-style: normal;
        font-weight: 800;
        font-size: 44px;
        line-height: 57px;
        color: #FFFFFF;
    }
</style>
