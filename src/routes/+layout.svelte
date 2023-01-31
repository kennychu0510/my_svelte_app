<script>
	import Footer from './Footer.svelte';
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<Footer/>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		height: 100vh;
	}
</style>
