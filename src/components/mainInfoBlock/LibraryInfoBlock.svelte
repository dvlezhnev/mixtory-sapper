<div class="wrap">
    <div class="container">
        <div class="block">
            <div class="container-poster">
                <div class="logo"></div>
            </div>
            <div class="container-text">
                <div class="text">Представьте, что вы играете в паззл. И как бы не переставляли его части, получается единая картина. Только каждый раз новая.</div>
                <div class="text">Mixtory — именно такой паззл. Перемешивайте предложения в случайном порядке и читайте каждый раз новую историю.</div>
            </div>
        </div>
    </div>
</div>

<style>
    .wrapper{
        background-color: #FFC700;
        background-image: url("/assets/main_library_text_things.svg");
    }
    .container{
        margin: auto;
        width: 1400px;
        padding: 0 120px;
        box-sizing: border-box;
    }

    .block{
        display: flex;
    }

    .block > .container-poster{
        width: 480px;
        height: 250px;
        background-color: #120D24;
        background-image:
            url("/assets/main_library_poster_things.svg"),
            url("/assets/main_library_poster.svg");
    }

    .block > .container-poster > .logo{
        background-image: url("/assets/main_library_poster_logo.svg");
        width: 100%;
        height: 100%;
        background-repeat: no-repeat;
        background-position: center;
    }

    .block > .container-text{
        padding: 64px 0 0 64px;
        flex: 1;
    }

    .block > .container-text > .text{
        font-style: normal;
        font-weight: 600;
        font-size: 17px;
        line-height: 25px;
        color: #120D24;
        margin-bottom: 25px;
    }
</style>
