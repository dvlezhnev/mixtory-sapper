<script>
    import Wrapper from "../common/wrapper/Wrapper.svelte";
    import ContentFrame from "../common/contentFrame/ContentFrame.svelte";
    import Logo from "./Logo.svelte";
    import LinksContainer from "./LinksContainer.svelte";

    export let segment;
</script>

<header>
    <Wrapper>
        <ContentFrame>
            <div class="row">
                <Logo/>
                <LinksContainer {segment}/>
            </div>
        </ContentFrame>
    </Wrapper>
</header>

<style>
    header {
        display: block;
    }
    .row {
        display: flex;
        justify-content: space-between;
    }
</style>
