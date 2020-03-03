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
    .wrapper{
        width: 100%;
    }
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
                font-size: 3.6rem;
                line-height: 4rem;
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
        @media (max-width: 1024px) {
            &{
                margin-top: 24px;
            }
        }
    }

    .info-block{
        padding: 96px 360px;
        @media (max-width: 1024px) {
            &{
                padding: 16px;
            }
        }
    }

    .info-block > .text{
        font-weight: 500;
        font-size: 20px;
        line-height: 30px;
        color: #120D24;
        margin-top: 20px;
        width: 620px;
        @media (max-width: 1024px) {
            &{
                width: auto;
            }
        }
    }

    .info-block > .text.bold{
        font-weight: 600;
    }
</style>
