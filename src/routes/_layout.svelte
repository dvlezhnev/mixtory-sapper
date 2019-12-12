<script>
	import Header from "../components/header/Header.svelte";
	import Footer from "../components/footer/Footer.svelte";

	export let segment;
</script>

<style>
	.main-container{
		box-sizing: border-box;
		min-height: calc(100vh - 80px - 175px);
	}
</style>

<Header {segment}/>
<div class="main-container">
	<slot></slot>
</div>
<Footer/>