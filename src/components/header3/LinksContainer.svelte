<script>
    let links = [
        {
            selected: "about",
            link: "about",
            text: "О проекте"
        },
        {
            selected: undefined,
            link: ".",
            text: "Библиотека"
        }
    ];

    export let segment;
</script>

<nav>
    {#each links as link}
        <a href="{link.link}" class:selected={segment === link.selected}>{link.text}</a>
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
