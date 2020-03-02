<script>
	import Header2 from "../components/header2/Header.svelte";
	import Footer2 from "../components/footer2/Footer.svelte";

	export let segment;
</script>

<Header2 {segment}/>
<main class="main-container">
	<slot/>
</main>
<Footer2/>

<style>
	main {
		box-sizing: border-box;
		min-height: calc(100vh - 80px - 123px);
	}
</style>
