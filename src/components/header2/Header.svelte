<script>
    import Link from "../common/a/Link.svelte";

    export let segment;

    let links = [
        {
            selected: undefined,
            link: ".",
            text: "Библиотека"
        },
        {
            selected: "about",
            link: "about",
            text: "О проекте"
        }
    ];
</script>
<section class="wrapper">
    <div class="container">
        <header>
            <a class="logo" href="."><span></span></a>
            <nav>
                {#each links as link}
                    <Link
                        link="{link.link}"
                        text="{link.text}"
                        selected="{segment === link.selected}"
                        font16="{true}"
                    />
                {/each}
            </nav>
        </header>
    </div>
</section>

<style type="text/scss">
    .wrapper{
        width: 100%;
        background-color: #ffffff;
    }

    .container{
        max-width: 1400px;
        margin: auto;
    }

    header{
        height: 80px;
        display: flex;
        box-sizing: border-box;
        align-items: center;
        justify-content: space-between;
    }

    .logo{
        width: 172px;
        height: 42px;
        background-image: url("/assets/logo.svg");
        background-repeat: no-repeat;
        background-size: contain;
        margin: auto 16px;
    }

    @media (max-width: 500px){
        header{
            flex-direction: column;
            height: auto;
            min-height: 100px;

            & > nav{
                margin: 24px auto;
            }
        }

        .logo{
            width: 172px;
            height: 42px;
            background-image: url("/assets/logo.svg");
            background-repeat: no-repeat;
            background-size: contain;
            margin: 1rem 0 0 0;
        }
    }
</style>
