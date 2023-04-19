<script>
	import Banner from './Components/Banner/Banner.svelte';

	
</script>

<div class="app">
	<Banner />

	<main>
		<slot />
	</main>

	
</div>

<style>
	.app {
		
		width: 100%;

        
	}

	main {
		
	}

	footer {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		padding: 12px;
		text-align: center;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}


    img {
        width: 2rem;
        padding: 1rem; 
    
       opacity: .7;
    }

    img:hover {
        background-color: rgb(0, 0, 0, .05);
       
        
    }
</style>
