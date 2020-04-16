<div class="wrapper">
    <div class="container">
        <div class="content">
            <div class="block-last">
                <h2 class="sub-title">Чуть не забыли уточнить, мы — это:</h2>
                <div class="container-persons">
                    <div class="person">
                        <div class="avatar elena"></div>
                        <div class="name">Елена Лопатина</div>
                        <div class="role">пишу истории</div>
                    </div>
                    <div class="person">
                        <div class="avatar denis"></div>
                        <div class="name">Денис Лежнев</div>
                        <div class="role">программирую истории</div>
                    </div>
                    <div class="person">
                        <div class="avatar ekaterina"></div>
                        <div class="name">Екатерина Зырянова</div>
                        <div class="role">рисую истории</div>
                    </div>
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
        padding: 0 16px;
    }

    .sub-title{
        display: block;
        text-align: center;
        margin-top: 72px;
        font-size: 32px;
        line-height: 46px;
        @media (max-width: 1024px) {
            &{
                font-size: 24px;
                line-height: 32px;
            }
        }
        @media (max-width: 500px) {
            &{
                margin-top: 36px;
            }
        }
    }

    .block-last > .container-persons{
        display: flex;
        padding-top: 88px;
        padding-bottom: 156px;

        @media (max-width: 500px) {
            &{
                flex-direction: column;
                padding-top: 36px;
                padding-bottom: 36px;
            }
        }
    }

    .block-last > .container-persons > .person{
        flex: 1;
        @media (max-width: 500px) {
            &{
                padding-bottom: 14px;
                &:last-child{
                    padding-bottom: 0;
                }
            }
        }
    }

    .block-last > .container-persons > .person > .avatar{
        width: 60px;
        height: 60px;
        background-color: #EBEBEB;
        border-radius: 50%;
        margin: auto;
        background-position: center;
        background-size: cover;
    }

    .avatar.elena{
        background-image: url("/assets/photo/lena.png");
    }
    .avatar.denis{
        background-image: url("/assets/photo/denis.png");
    }
    .avatar.ekaterina{
        background-image: url("/assets/photo/ekaterina.png");
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
