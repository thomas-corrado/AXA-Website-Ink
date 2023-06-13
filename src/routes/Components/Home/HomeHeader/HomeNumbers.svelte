<script>

    const metrics = new Set([['Members', '96'], ['GPA', '4.0'], ['Years Active', '60']]);
	
</script>


<header>
	<link rel="stylesheet" href="https://use.typekit.net/dlr4khc.css">
	
	
	<div class="landing-info-outer">
		
            <br>
            <br>
			<h2>
				AXA in Numbers
			</h2>
			<br>
            
            <div class="orientation-outer">
                
                    {#each [...metrics] as item}
                        <div class="orientation-inner">
                        <h3>
                            {item[1]}
                        </h3>

                        <br>

                        <h4>
                            {item[0]}
                        </h4>
                           
						</div>
			        {/each}
             
                      
			
		</div>

        <br>
                      <br> 
	</div>	
</header>

<style>

	.landing-info-outer {
		background-color: #F4F4F4;
		width: 100vw;
		margin: 0;
		padding: 0;
		justify-content: center;
		display: flex;
        flex-direction: column;
        align-items: center;
	}

     .orientation-outer {
        width: 30rem;
        display: flex;
        align-items: center;
        flex-direction: row;

        position: relative;
        padding-top: 3px;
    }

    .orientation-inner {
         width: 100vw;
        display: flex;
        align-items: center;
        flex-direction: column;
        position: relative;
    }

    h2 {
        text-align: center;
       position: relative;
	   font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		margin: 0; 
		padding: 0; 
        font-size: 3.5rem;
    }

    h3 {
		
		 text-align: center;
       position: relative;
	   font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		margin: 0; 
		padding: 0; 
        font-size: 2.5rem;
        color: #AA1717;
	}

	h4 {
		
		 text-align: center;
       position: relative;
	   font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		margin: 0; 
		padding: 0; 
        font-size: 1.5rem;
	}

   

    @media (max-width: 660px) {

        h2 {
            font-size: 2.5rem;
        }
   .orientation-outer {
        flex-direction: column;
        margin-top: -2rem;
  }

  .orientation-inner {
        padding-top: 2rem;
    }
}
	
</style>
