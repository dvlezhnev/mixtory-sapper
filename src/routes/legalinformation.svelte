<svelte:head>
    <title>Правовая информация</title>
</svelte:head>
<div class="wrapper">
    <div class="container">
        <h1 class="title">Правовая информация</h1>
        <h2 class="sub-title">Условия использования<br>материалов сайта mixtory.ru</h2>
        <div class="rules">
            <div class="rule">1. Любое использование материалов сайта mixtory.ru (далее — Сайт), в частности, текстов и иллюстраций, допускается на оговорённых ниже условиях. Под использованием понимается любое воспроизведение, опубликование, копирование, перепечатывание, распространение, перевод, передача в эфир, сообщение по кабелю, переработка и другие способы, предусмотренные действующим законодательством Российской Федерации.</div>
            <div class="rule">2. Частичное или полное использование текстов Сайта разрешается только при условии ссылки и/или прямой открытой для поисковых систем гиперссылки на непосредственный адрес материала на Сайте. Размер шрифта ссылки или гиперссылки не должен быть меньше шрифта текста используемого материала. Ссылка/гиперссылка обязательна вне зависимости от полного или частичного использования материалов.</div>
            <div class="rule">3. Использование иллюстраций Сайта без привязки к текстам Сайта запрещается.</div>
            <div class="rule">4. Использование материалов сайта в коммерческих целях возможно только с письменного разрешения владельцев авторских прав. Для связи с авторами пишите на hello@mixtory.ru</div>
            <div class="rule">5. Нарушение вышеуказанных условий будет расцениваться как нарушение защищаемых законом авторских прав и прав на интеллектуальную собственность. В таких случаях администрация сайта и авторы материалов оставляют за собой право на защиту прав в судебном порядке в соответствии с законодательством Российской Федерации.</div>
            <div class="rule">6. Администрация сайта имеет право в любое время вносить изменения в настоящие условия. Изменения вступают в силу с момента опубликования новой редакции на Сайте.</div>
        </div>
    </div>
</div>
<div class="wrapper" style="background-color: #E9FFF3;">
    <div class="container">
        <div class="info-block">
            <div class="text bold">Для тех, кто никогда не читает условия и соглашения, коротко:</div>
            <div class="text bold">Вы можете публиковать наши истории и читать их вслух, где хотите, если не собираетесь зарабатывать на них. Но не забывайте при этом ссылаться на mixtory.ru. Иначе мы обидимся и наведём на вас порчу.</div>
            <div class="text bold">Приятного чтения!</div>
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
        font-weight: 600;
        font-size: 32px;
        line-height: 46px;
        color: #120D24;
        @media (max-width: 1024px) {
            &{
                font-size: 2rem;
                line-height: 2.2rem;
            }
        }
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

    .rules{
        padding: 45px 320px;
        @media (max-width: 1024px) {
            &{
                padding: 16px;
            }
        }
    }

    .rules > .rule{
        font-style: normal;
        font-weight: 500;
        font-size: 17px;
        line-height: 25px;
        color: #120D24;
        margin-bottom: 25px;
    }

    .info-block{
        padding: 96px 320px;
        @media (max-width: 1024px) {
            &{
                padding: 16px;
            }
        }
    }

    .info-block > .text{
        font-style: normal;
        font-weight: bold;
        font-size: 17px;
        line-height: 25px;
        color: #120D24;
        margin-bottom: 25px;
    }

    .info-block > .text.bold{
        font-weight: 600;
    }
</style>
