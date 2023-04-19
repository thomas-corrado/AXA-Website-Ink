<script>
 import HomeHeader from "./Components/HomeHeader/HomeHeader.svelte";

 
</script>

<svelte:head>
	<title>AXA | Home</title>
	<meta name="description" content="Alpha Chi Alpha Homepage" />
</svelte:head>

<section>
	<div class='home-wrapper'>
		<HomeHeader/>

	</div>
	
	

</section>

<style>

	section {
		width: 100%;
height: 100%;
	}

	.home-wrapper {
		width: 100%; 
		display: flex;
		flex-direction: column;
		align-items: center;
	}


</style>