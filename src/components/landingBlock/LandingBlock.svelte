<section class="wrapper">
    <div class="container">
        <div class="content">
            <div class="poster">
                <div class="logo"></div>
            </div>
            <div class="info">
                <div class="text">Mixtory — это библиотека коротких историй с текучим сюжетом. Истории состоят из карточек, которые можно мешать в случайном порядке хоть квинтиллион раз. При любом раскладе получается целостный текст.</div>
                <div class="text">Но каждый раз на первый план выходят то одни, то другие детали. Вплоть до того, что герои и события могут оказаться вовсе не такими, какими представлялись при первом прочтении.</div>
            </div>
        </div>
    </div>
</section>

<style type="text/scss">
    .wrapper{
        background-color: #EFEDF6;
        background-image: url("/assets/main_library_text_things.svg");
    }

    .container{
        max-width: 1400px;
        margin: auto;
        padding: 0 120px;
        box-sizing: border-box;
    }

    .content{
        width: 100%;
        display: flex;
    }

    .poster{
        flex-grow: 5;
        flex-basis: 0;
        min-height: 250px;
        position: relative;
        background-color: #120D24;
        background-image:
                url("/assets/main_library_poster_things.svg"),
                url("/assets/main_library_poster.svg");
        background-repeat: repeat-y;
        background-size: cover;

        & > .logo{
            background-image: url("/assets/main_library_poster_logo.svg");
            width: 100%;
            height: 100%;
            background-repeat: no-repeat;
            background-position: center;
        }
    }

    .info{
        flex-grow: 7;
        flex-shrink: 0;
        flex-basis: 0;
        box-sizing: border-box;

        & > .text{
            font-style: normal;
            font-weight: 600;
            font-size: 17px;
            line-height: 25px;
            color: #120D24;
            margin-top: 25px;
            margin-bottom: 25px;
            margin-left: 64px;

            &:first-child{
                margin-top: 64px;
            }

            &:last-child{
                margin-bottom: 64px;
            }
        }
    }

    @media (max-width: 1024px) {
        .container{
            padding: 0;
        }
        .content{
            flex-direction: column;
        }
        .poster{
            flex-grow: 1;
            height: 250px;
        }
        .info{
            flex-grow: 1;
            padding: 0 36px;

            & > .text{
                margin-left: 0;
            }
        }
    }
</style>
