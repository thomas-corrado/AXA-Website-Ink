<svelte:head>
	<title>AXA | On Campus</title>
	<meta name="description" content="Alpha Chi Alpha On Campus" />
</svelte:head>

<script>
	import GeneralHeader from "../Components/GeneralHeader.svelte";

</script>

<section>
<div class="on-campus">

	<div>
		<GeneralHeader image_string="https://axa-website-ink.s3.amazonaws.com/AXA_ND2_copy.jpg" alt_text="Men standing on roof picture" header_text="On Campus" margin_top_val="15rem"/> 
	</div>

	
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

	.on-campus { 
		width: 100%; 
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0;
		padding: 0;
	}

</style>
