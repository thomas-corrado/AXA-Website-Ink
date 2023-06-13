<script>
 import HomeHeader from "./Components/Home/HomeHeader/HomeHeader.svelte";
 import HomeInfo from "./Components/Home/HomeHeader/HomeInfo.svelte";
 import HomeNumbers from "./Components/Home/HomeHeader/HomeNumbers.svelte";

 
</script>

<svelte:head>
	<title>AXA | Home</title>
	<meta name="description" content="Alpha Chi Alpha Homepage" />
</svelte:head>

<section>
	<div class='home-wrapper'>
		<HomeHeader/>
		<HomeInfo/>
		<HomeNumbers/>

	</div>
	
	

</section>

<style>

	

	section {
		width: 100%;
		height: 100%;
		margin: 0;
		padding: 0;
		display: flex;
		
	}

	.home-wrapper {
		width: 100%; 
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0;
		padding: 0;
		
	}


</style>