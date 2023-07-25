


<script>

     /**
	 * @type {Array<any>}
	 */
    export let axa_class_year; 
	


</script>

<section>
<div>

		<div id="grid">
			{#each [...axa_class_year] as { image_url, name, position }}
      			<div>
					
			<div class="portrait-container">
					<img src={image_url} alt='{name}' />
				</div>
				<h3>
						{name}
					</h3>
					
					<h4>
						{position}
					</h4>
					
				</div>
				
  			{/each}
    </div>


</div>
</section>


<style>

	section {
		
		margin: 0;
		padding: 0;

	}

	h3 {
		text-align: center;
		font-size: 1.75rem;
		font-style: normal;
		font-weight: 200;
		padding-top: 1.25rem;
		padding-bottom: 4px;
		margin: 0;
	}

	h4 { 
		text-align: center;
		font-size: 1.25rem;
		font-style: normal;
		font-weight: 200;
		padding: 3px;
		margin: 7px;
	}

	#grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        grid-gap: 20px;
		
      }
      #grid > div {
        font-size: 30px;
        padding: .5em;
        color: black;
        
        text-align: center;
      }
	  
	.portrait-container { 
		 width: 100%;
         height: 20rem;
        overflow: hidden;
        display: grid;
       text-align: center;
       position: relative;
       place-items: center;
	   
	}

	.portrait-container img { 
		width: 100%;
    height: 100%;
    object-fit: cover;
    overflow: hidden;
	}
	

</style>
