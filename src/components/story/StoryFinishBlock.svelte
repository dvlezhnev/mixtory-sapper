<script>
    import { createEventDispatcher } from 'svelte';
    export let countVariant;

    const dispatch = createEventDispatcher();
    function remix() {
        dispatch("remix", {});
    }
    function share() {
        dispatch("share", {});
    }

    let isAndroid = false;
    if (/Android/.test(navigator.userAgent))
    {
        isAndroid = true;
    }

    let shareAvailable = !!navigator.share;

</script>

<div class="info">
    <span>Вы только что прочитали</span>
    <span class="big">1</span>
    <span>из возможных</span>
    <span class="big">{countVariant}</span>
    <span>вариантов развития истории</span>
</div>
<div class="finished-buttons-container">
        <div class="share-button-container">
        {#if shareAvailable}
            <button class="share-button" on:click={share}><span class="share-icon" class:ios={!isAndroid} class:android={isAndroid}></span><span class="share-button-text">Поделиться</span></button>
        {/if}
        </div>
    <div class="action-button-container">
        <button class="remix" on:click={remix}>Перемешать заново</button>
        <a href=".">Выбрать другую историю →</a>
    </div>
</div>

<style type="text/scss">
    .info {
        box-sizing: border-box;
        display: flex;
        align-items: center;
        justify-content: space-between;

        @media (max-width: 1024px) {
            & {
                flex-direction: column;
            }
        }
    }

    .info > span{
        font-family: Merriweather, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 15px;
        line-height: 19px;
        color: #120D24;
    }

    .info > span.big{
        font-family: Montserrat, sans-serif;
        font-weight: 500;
        font-size: 38px;
        line-height: 53px;
        color: #120D24;

        @media (max-width: 1024px) {
            & {
                font-size: 28px;
            }
        }
    }

    .finished-buttons-container{
        padding-top: 2rem;
        display: flex;
        justify-content: space-between;

        @media (max-width: 1024px) {
            & {
                flex-direction: column;
            }
        }
    }

    .finished-buttons-container  button{
        background-color: #ffffff;
        color: #120D24;
    }

    .finished-buttons-container  a{
        display: inline-block;
        padding: 20px;
        font-weight: 600;
        font-size: 16px;
        line-height: 18px;
        color: #FFFFFF;
        background: #22C06B;
        border-radius: 4px;
        border: 4px solid #22C06B;
        cursor: pointer;
        text-decoration: none;
        margin-left: 32px;
        box-sizing: border-box;

        @media (max-width: 1024px) {
            & {
                flex-direction: column;
                margin-left: 0;
                margin-top: 1rem;
                width: 100%;
            }
        }
    }
    button.remix{
        padding: 20px;
        font-weight: 600;
        font-size: 16px;
        line-height: 18px;
        border-radius: 4px;
        border: 4px solid #22C06B;
        cursor: pointer;
        @media (max-width: 1024px) {
            & {
                width: 100%;
            }
        }
    }

    .share-icon{
        width: 40px;
        height: 40px;
        display: inline-block;
        border-radius: 50%;
        background-color: #DAF3E7;
        margin-right: 16px;
        &.ios {
            background-image: url("/assets/share_ios.svg");
            background-size: 24px;
            background-position: center;
            background-repeat: no-repeat;
        }
        &.android {
            background-image: url("/assets/share_android.svg");
            background-size: 24px;
            background-position: center;
            background-repeat: no-repeat;
        }
    }
    .share-button {
        display: inline-flex;
        align-items: center;
        border: none;
        cursor: pointer;
        font-weight: 600;
        font-size: 16px;
        line-height: 24px;
    }
    .share-button-text {
        font-weight: 600;
        font-size: 16px;
        line-height: 24px;
        color: #120D24;
    }
    .share-button-container {
        align-self: center;

        @media (max-width: 1024px) {
            & {
                margin-top: 1rem;
                margin-bottom: 2rem;
            }
        }
    }
</style>
