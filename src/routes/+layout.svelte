<script>
	import Banner from './Components/Banner/Banner.svelte';
	import Footer from './Components/Footer/Footer.svelte';

	

	
</script>

<div class="app" data-sveltekit-preload-data>
	<Banner />

	<main>
		<slot />
	</main>

	<Footer/> 
</div>

<style>

	

	:root {

		height: 0;
		width: 100%;
		overflow-x: hidden;
		margin: 0; 
		padding: 0;
		
}


	.app {
		width: 100%; 
		
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0;

	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;	
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
	

	}

	
</style>
