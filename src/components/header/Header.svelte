<script>
    export let segment;
</script>

<div class="wrap">
    <div class="container">
        <div class="main-header">
            <div class="logo"></div>
            <div class="container-links">
                <a class:selected='{segment === undefined}' href=".">Библиотека</a>
                <a class:selected='{segment === "about"}' href="about">О проекте</a>
            </div>
        </div>
    </div>
</div>

<style>
    .container{
        max-width: 1400px;
        margin: auto;
    }

    .main-header{
        display: flex;
        width: 100%;
        height: 80px;
        padding-left: 32px;
        padding-right: 32px;
        box-sizing: border-box;
        align-items: center;
        background: #ffffff;
    }

    .main-header > *{
        display: inline-block;
    }

    .main-header > .logo{
        width: 172px;
        height: 42px;
        background-image: url("/assets/logo.svg");
        background-repeat: no-repeat;
        background-size: contain;
    }

    .main-header > .container-links{
        flex: 1;
        text-align: right;
    }

    a{
        display: inline-block;
        font-weight: 600;
        font-size: 16px;
        line-height: 23px;
        color: #120D24;
        text-decoration: none;
        margin-left: 48px;
    }

    a.selected{
        color: #22C06B;
    }
</style>