<script>
	import StoryList from "../components/storyList/StoryList.svelte";
	import {stories} from "./stories/_stories";
	import LandingBlock from "../components/landingBlock/LandingBlock.svelte";
</script>
<style>

</style>

<svelte:head>
	<title>Mixtory — библиотека коротких историй со случайным сюжетом</title>
	<meta name='theme-color' content='#120D24'>
	<meta name="apple-mobile-web-app-status-bar-style" content="#120D24">
	<meta property="og:locale" content="ru_RU"/>
	<meta property="og:type" content="article"/>
	<meta property="og:title" content="Mixtory - случайное случается!"/>
	<meta property="og:description" content="Мешайте предложения в случайном порядке хоть квинтиллион раз и читайте целую историю при любом раскладе."/>
	<meta name="description" content="Мешайте предложения в случайном порядке хоть квинтиллион раз и читайте целую историю при любом раскладе."/>
	<meta property="og:image" content="https://mixtory.ru/assets/share_covers/mixtory.jpg"/>
	<meta property="og:image:width" content="751"/>
	<meta property="og:image:height" content="392"/>
	<meta property="vk:image" content="https://mixtory.ru/assets/share_covers/mixtory.jpg"/>
	<meta property="og:url" content="https://mixtory.ru/"/>
	<meta property="og:site_name" content="Mixtory"/>
</svelte:head>

<LandingBlock/>
<StoryList title="Выберите историю" stories="{stories}"/>
