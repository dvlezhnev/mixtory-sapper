<script>
    import Link from "../common/a/Link.svelte";

    let links = [
        {
            selected: "about",
            link: "about",
            text: "О проекте"
        },
        {
            selected: "legalinformation",
            link: "legalinformation",
            text: "Правовая информация"
        },
        {
            selected: undefined,
            link: ".",
            text: "Библиотека"
        },
        {
            selected: undefined,
            link: "mailto:hello@mixtory.ru",
            text: "hello@mixtory.ru"
        }
    ];
</script>

<section class="wrapper">
    <div class="container">
        <footer>
            <nav>
                {#each links as link}
                    <Link
                        link="{link.link}"
                        text="{link.text}"
                    />
                {/each}
            </nav>
            <div class="copyright">
                © 2019 - 2020, Mixtory
            </div>
        </footer>
    </div>
</section>

<style type="text/scss">
    .wrapper{
        width: 100%;
        border-top: 1px solid #CDCAD6;
    }

    .container{
        max-width: 1400px;
        margin: auto;
    }

    footer{
        padding-bottom: 16px;
    }

    nav{
        margin-top: 36px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .copyright{
        font-style: normal;
        font-weight: normal;
        font-size: 1rem;
        line-height: 20px;
        text-align: center;
        color: #252132;
        margin-top: 32px;
    }

    @media (max-width: 500px) {
        nav{
            flex-direction: column;
        }
    }
</style>
