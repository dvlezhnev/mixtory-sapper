<script>
    export let segment;
</script>

<div class="wrap">
    <div class="container">
        <div class="nav">
            <div class="logo"></div>
            <div class="container-links">
                <a class:selected='{segment === undefined}' href=".">Библиотека</a>
                <a class:selected='{segment === "about"}' href="about">О проекте</a>
            </div>
        </div>
    </div>
</div>

<style type="text/scss">
    .wrapper{
        width: 100%;
    }

    @media screen and (max-width: 575.98px){
        .container {
            width: 100%;
        }
    }
    .container{
        width: 1400px;
        margin: auto;
    }

    .nav{
        display: flex;
        width: 100%;
        height: 80px;
        box-sizing: border-box;
        background: #ffffff;
        align-items: center;
        justify-content: space-between;

        & > .logo{
            width: 172px;
            height: 42px;
            background-image: url("/assets/logo.svg");
            background-repeat: no-repeat;
            background-size: contain;
        }
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
