<script>
	import Footer from "../components/footer/Footer.svelte";
	import Header2 from "../components/header2/Header.svelte";

	export let segment;
</script>

<Header2 {segment}/>
<main class="main-container">
	<slot/>
</main>
<Footer/>

<style>
	main {
		box-sizing: border-box;
		min-height: calc(100vh - 80px - 175px);
	}
</style>
