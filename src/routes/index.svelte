<script>
	import LibraryInfoBlock from "../components/mainInfoBlock/LibraryInfoBlock.svelte";
	import StoryList from "../components/storyList/StoryList.svelte";
	import {stories} from "./stories/_stories";
</script>
<style>

</style>

<svelte:head>
	<title>Mixtory - Библиотека</title>
</svelte:head>

<LibraryInfoBlock/>
<StoryList title="Выберите историю" stories="{stories}"/>