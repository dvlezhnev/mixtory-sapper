<script>
    export let text = "Ссылка";
    export let link = ".";
    export let selected = false;
    export let bold = true;
    export let font16 = false;
</script>

<a
    class:selected={selected}
    class:bold={bold}
    class:font16={font16}
    href='{link}'
>{text}</a>

<style type="text/scss">
    a {
        text-decoration: none;
        margin: auto 16px;
        font-size: 1rem;
        color: #120D24;

        &.selected{
            color: #22C06B;
        }

        &.bold{
            font-weight: 600;
        }

        &.font16{
            font-size: 16px;
        }
    }
</style>
