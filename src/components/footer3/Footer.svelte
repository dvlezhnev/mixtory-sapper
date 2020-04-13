<script>
    import Wrapper from "../common/wrapper/Wrapper.svelte";
    import ContentFrame from "../common/contentFrame/ContentFrame.svelte";
    import Copyright from "./Copyright.svelte";
    import LinksContainer from "./LinksContainer.svelte";

    const borderTop = true;
</script>

<footer>
    <Wrapper {borderTop}>
        <ContentFrame>
            <LinksContainer/>
            <Copyright/>
        </ContentFrame>
    </Wrapper>
</footer>

<style type="text/scss">
    footer {
        width: 100%;
    }
</style>
