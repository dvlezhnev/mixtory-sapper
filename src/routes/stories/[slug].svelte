<script context="module">
    import {stories} from "./_stories";
    export async function preload({ params, query }) {
        let story = stories.find(s => s.slug === params.slug);
        if (story)
            return { story };
        else
            this.error(404, "Нет такой истории");
    }
</script>

<script>
    import StoryBlock from "../../components/story/StoryBlock.svelte";

    export let story;
</script>

<StoryBlock story="{story}"/>
