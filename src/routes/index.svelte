<script>
	import LibraryInfoBlock from "../components/mainInfoBlock/LibraryInfoBlock.svelte";
	import StoryList from "../components/storyList/StoryList.svelte";
	import {stories} from "./stories/_stories";
	import LandingBlock from "../components/landingBlock/LandingBlock.svelte";
</script>
<style>

</style>

<svelte:head>
	<title>Mixtory - Библиотека</title>
</svelte:head>

<LandingBlock/>
<StoryList title="Выберите историю" stories="{stories}"/>
