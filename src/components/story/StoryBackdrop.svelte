<script>
    export let story;
    let defaultBackdropColor = "rgba(18,13,36,1)";
    let backdropAssetPath = "/assets/covers/";

    let backdropColor = story.backdropColor? story.backdropColor : defaultBackdropColor;
    let backdropCover = story.cover ? `url("${backdropAssetPath + story.cover}")` : "none";
</script>

<div class="backdrop" style="background-color: {backdropColor}">
    <div class="cover" style="background-image: {backdropCover}"></div>
</div>

<style type="text/scss">
    .backdrop{
        width: 100%;
        height: 50%;
        position: absolute;
        z-index: -1;
    }
    .cover{
        width: 100%;
        height: 100%;
        position: relative;
        background-repeat: repeat;
        background-position-x: -10px;
    }
</style>
