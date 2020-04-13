<script>
    export let borderBottom = false;
    export let borderTop = false;
    export let backgroundColor = "none";
</script>

<section class="wrapper"
         class:border-bottom={borderBottom}
         class:border-top={borderTop}
         style="background-color: {backgroundColor}">
    <slot/>
</section>

<style>
    section {
        width: 100%;
        padding: 0;
        margin: 0;
    }

    section.border-bottom {
        border-bottom: 1px solid #CDCAD6;
    }

    section.border-top {
        border-top: 1px solid #CDCAD6;
    }
</style>
