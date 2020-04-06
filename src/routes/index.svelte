<script>
	import StoryList from "../components/storyList/StoryList.svelte";
	import {stories} from "./stories/_stories";
	import LandingBlock from "../components/landingBlock/LandingBlock.svelte";
</script>
<style>

</style>

<svelte:head>
	<title>Mixtory - Библиотека</title>
	<meta property="og:locale" content="ru_RU"/>
	<meta property="og:type" content="article"/>
	<meta property="og:title" content="Mixtory - случайное случается!"/>
	<meta property="og:description" content="Замиксуйте свою версию истории!"/>
	<meta property="og:image" content="https://mixtory.ru/assets/share_covers/index.jpg"/>
	<meta property="vk:image" content="https://mixtory.ru/assets/share_covers/index.jpg"/>
	<meta property="og:url" content="https://mixtory.ru/"/>
	<meta property="og:site_name" content="Mixtory"/>
</svelte:head>

<LandingBlock/>
<StoryList title="Выберите историю" stories="{stories}"/>
