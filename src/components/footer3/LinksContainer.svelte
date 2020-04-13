<script>
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
        }
    ];
</script>

<nav>
    {#each links as link}
        <a href="{link.link}">{link.text}</a>
    {/each}
</nav>

<style type="text/scss">
    nav {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }
    a {
        display: inline-block;
        font-size: 1rem;
    }
</style>
