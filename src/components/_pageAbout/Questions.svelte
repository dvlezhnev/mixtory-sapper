<div class="wrapper">
    <div class="container">
        <div class="content">
            <div class="block-first">
                <h1 class="title">О проекте</h1>
                <h2 class="sub-title" style="margin-top: 16px;">Однажды мы подумали</h2>
                <div class="questions">
                    <div class="row">
                        <div class="question question-1">
                            <div class="icon">😜</div>
                            <div class="text">«А не сочинить ли истории со случайным сюжетом?»</div>
                        </div>
                        <div class="question question-2">
                            <div class="icon">🙀</div>
                            <div class="text">«Так, чтобы их составные части можно было мешать в любом порядке.»</div>
                        </div>
                    </div>
                    <div class="question question-3">
                        <div class="icon">😲</div>
                        <div class="text">«И чтобы каждая история звучала как связный текст при любом раскладе.»</div>
                    </div>
                </div>
                <div class="stickers-block">
                    <div class="stickers"></div>
                    <div class="text">Вскоре появились первые экземпляры на цветных стикерах. А потом эти стикеры превратились в Mixtory — онлайн-генератор историй со случайным сюжетом.</div>
                </div>
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
    }

    .questions{
        text-align: center;
        padding-left: 16px;
        padding-right: 16px;
    }

    .questions > .row
    {
        margin-top: 36px;
        margin-bottom: 36px;
        @media (min-width: 1180px){
            &{
                margin-top: 100px;
                margin-bottom: 100px;
            }
        }

    }

    .questions  .question{
        max-width: 560px;
        width: 100%;
        height: 290px;
        margin: auto;
        text-align: center;
        box-sizing: border-box;
        background-repeat: no-repeat;
        background-size: contain;
        background-position: center;
        display: inline-flex;
        flex-direction: column;
        align-content: center;
        justify-content: center;

        @media (max-width: 500px) {
            height: auto;
        }
    }

    .questions  .question.question-1{
        background-image: url("/assets/question_1.svg");
        margin-bottom: 36px;
        @media (min-width: 1180px){
            &{
                transform: translateY(-50px);
                margin-right: 20px;
                margin-bottom: 0;
            }
        }

        @media (max-width: 500px) {
            background-image: none;
        }
    }
    .questions  .question.question-2{
        background-image: url("/assets/question_2.svg");
        @media (min-width: 1180px){
            transform: translateY(50px);
            margin-left: 20px;
        }
        @media (max-width: 500px) {
            background-image: none;
        }
    }
    .questions  .question.question-3{
        background-image: url("/assets/question_3.svg");
        @media (max-width: 500px) {
            background-image: none;
        }
    }

    .questions  .question > .icon{
        font-size: 40px;
        font-weight: 600;
        @media (max-width: 500px) {
            font-size: 36px;
        }
    }

    .questions  .question > .text{
        font-style: normal;
        font-weight: 500;
        font-size: 20px;
        line-height: 26px;
        color: #120D24;
        width: 90%;
        margin-left: auto;
        margin-right: auto;
        @media (max-width: 500px) {
            font-size: 16px;
            line-height: 20px;
        }
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
        max-width: 430px;
        margin: auto;
    }

    .stickers-block > .text{
        max-width: 686px;
        margin: 32px auto 0 auto;
        font-style: normal;
        font-weight: 500;
        font-size: 20px;
        line-height: 30px;
        text-align: center;
        color: #120D24;
        padding: 0 16px;
    }
</style>
