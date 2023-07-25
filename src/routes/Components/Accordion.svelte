<script>
  export let open = false;
	import { slide } from 'svelte/transition';
	const handleClick = () => open = !open
</script>

<div class="accordion">
	<div class="header">
		<button on:click={handleClick} >
			
			<div class="text">
				{#if open}
				<div class="arrow">
					&gt; 
				</div>
				{:else}
				&gt; 
				{/if}
				
				<div class="header-text">
					<slot name="head" ></slot>	
				</div>
				
			</div>
		</button>
		
		
		
	</div>
	
	{#if open}
	<div class="details" transition:slide>
		<slot name="details">
		</slot>
	</div>
	{/if}
</div>

<style>
	.accordion {
		width: 100vw; 
	}
	
	.header {
		display:flex;
		width:100%;
		
	}

	.header button {
		background-color: transparent;
		border: none;
		font-size: calc(.75vw + 1.5rem);
		position: relative;
		display: flex;
		padding: 5px;
		padding-left: 25px;
		width: 100%;
		
	}

	@media screen and (max-width: 600px) {
  .header button {
		
		padding-left: 20px;
		
	}}
	
	.header .text {
		flex: 1;
		margin-right: 5px;
		font-size: calc(1.5vw + 2.75rem);
		position: relative;
		display: flex;
		align-items: flex-start;
		text-align: left;
		font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		color: black;
		padding: 0;
	}

	.header-text {
		padding-left: 7px;
		position: relative;
	}

	.arrow { 
		transform: rotate(90deg);
		left: 4px;
		position: relative;
	}
	
	.details {
		position: relative;
		display: flex;
		width: 100vw;
		justify-content: center;
	}
</style>
