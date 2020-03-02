<div class="wrapper" style="background-color: #FFF9E5;">
    <div class="container">
        <div class="content">
            <div class="info-block">
                <h2>Как это работает?</h2>
                <div class="text">Всё дело в том, что человеческий мозг стремится найти связи даже там, где они неочевидны. Стоит только подкинуть ему что-то знакомое, как он уже вытаскивает одну за другой ассоциации.</div>
                <div class="text bold">Эти ассоциации, помимо специальных синтаксических уловок, и связывают карточки друг с другом.</div>
            </div>
        </div>
    </div>
</div>
<div class="wrapper" style="background-color: #ffffff;">
    <div class="container">
        <div class="content">
            <div class="info-block">
                <h2>Почему карточки?</h2>
                <div class="text">Для рождения ассоциаций нужно время — буквально полсекунды. Поэтому мы и выбрали формат сменяющих друг друга карточек, а не сплошной текст.  В момент смены карточек рождаются связи, и случайный порядок фраз становится закономерным.</div>
                <div class="text bold">Паузы в таком деле играют не менее важную роль, чем слова.</div>
            </div>
        </div>
    </div>
</div>
<div class="wrapper" style="background-color: #E9FFF3;">
    <div class="container">
        <div class="content">
            <div class="info-block">
                <h2>Как читать?</h2>
                <div class="text">Замечено, что при втором, третьем и последующих прочтениях одной и той же истории она выглядит всё более цельной.</div>
                <div class="text">А если мешать карточки в компании друзей, когда каждый читает их в своём порядке, со своими интонациями, то случайно может возникнуть совершенно неожиданный подтекст.</div>
                <div class="text bold">Мы уже пробовали — теперь ваша очередь.</div>
            </div>
        </div>
    </div>
</div>

<style type="text/scss">
    .container{
        max-width: 1400px;
        margin: auto;
    }

    .content{
        max-width: 1400px;
    }

    h1{
        font-style: normal;
        font-weight: 900;
        font-size: 60px;
        line-height: 87px;
        color: #120D24;

        @media (max-width: 1024px) {
            &{
                font-size: 4rem;
                line-height: 4.2rem;
            }
        }
    }

    h2{
        font-style: normal;
        font-weight: 500;
        font-size: 20px;
        line-height: 30px;
        color: #120D24;
    }

    .title{
        display: block;
        text-align: center;
        margin-top: 48px;

        @media (max-width: 1024px) {
            &{
                margin-top: 0;
            }
        }
    }

    .sub-title{
        display: block;
        text-align: center;
        margin-top: 72px;
    }

    .info-block{
        padding: 96px 360px;
    }

    .info-block > .text{
        font-weight: 500;
        font-size: 20px;
        line-height: 30px;
        color: #120D24;
        margin-top: 20px;
        width: 620px;
    }

    .info-block > .text.bold{
        font-weight: 600;
    }

    .questions{
        text-align: center;
    }

    .questions  .question{
        width: 560px;
        height: 290px;
        margin: auto;
        text-align: center;
        padding: 57px 140px;
        box-sizing: border-box;
        background-repeat: no-repeat;
        display: inline-block;
    }

    .questions  .question.question-1{
        background-image: url("/assets/question_1.svg");
        transform: translateY(-50px);
        margin-right: 20px;
    }
    .questions  .question.question-2{
        background-image: url("/assets/question_2.svg");
        transform: translateY(50px);
        margin-left: 20px;
    }
    .questions  .question.question-3{
        background-image: url("/assets/question_3.svg");
        display: block;
    }

    .questions  .question > .icon{
        font-size: 40px;
        font-weight: 600;
    }

    .questions  .question > .text{
        font-style: normal;
        font-weight: 500;
        font-size: 20px;
        line-height: 26px;
        color: #120D24;
    }

    .stickers-block{
        padding: 104px 0;
        box-sizing: border-box;
    }

    .stickers-block > .stickers{
        background-image: url("/assets/stickers.svg");
        background-repeat: no-repeat;
        background-size: contain;
        height: 200px;
        width: 430px;
        margin: auto;
    }

    .stickers-block > .text{
        width: 654px;
        margin: 32px auto 0 auto;
        font-style: normal;
        font-weight: 500;
        font-size: 20px;
        line-height: 30px;
        text-align: center;
        color: #120D24;
    }

    .block-last{

    }

    .block-last > .container-persons{
        display: flex;
        padding-top: 88px;
        padding-bottom: 156px;
    }

    .block-last > .container-persons > .person{
        flex: 1;
    }

    .block-last > .container-persons > .person > .avatar{
        width: 60px;
        height: 60px;
        background: #EBEBEB;
        border-radius: 50%;
        margin: auto;
    }

    .block-last > .container-persons > .person > .name{
        font-style: normal;
        font-weight: 600;
        font-size: 17px;
        line-height: 25px;
        text-align: center;
        color: #120D24;
        margin: 24px 0 0 0;
    }

    .block-last > .container-persons > .person > .role{
        font-style: normal;
        font-weight: 500;
        font-size: 17px;
        line-height: 25px;
        text-align: center;
        color: #120D24;
        margin: auto;
    }
</style>
