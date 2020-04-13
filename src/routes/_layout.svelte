<script>
	import Footer from "../components/footer3/Footer.svelte";
	import Header from "../components/header3/Header.svelte";

	export let segment;
</script>

<Header {segment}/>
<main class="main-container">
	<slot/>
</main>
<Footer/>

<style>
	main {
		flex-grow: 1;
	}
</style>
