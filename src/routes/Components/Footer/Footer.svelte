<script>

    const pages = new Set([['HOME', ''], ['ON CAMPUS', 'oncampus'], ['HISTORY', 'history'], ['ALUMNI', 'alumni'],['CONTACT', 'contact'], ['DONATE', 'donate']]);
	
</script>


<header>
	<link rel="stylesheet" href="https://use.typekit.net/dlr4khc.css">
	
	
	<div class="union">
        

        <div class="orientation">
            
            <div class="address">
                <br>
                <h4>
                    Alpha Chi Alpha Fraternity 
                </h4>
                <h6>
                    13 Webster Avenue 
                    Hanover, NH 03755
                </h6>
               
            </div>
            

            {#each [...pages] as item}
       
                    <a href='/{item[1] !== '' ? item[1] : ''}'>{item[0]}</a>
                    
        
			{/each}
            

            
        </div>
        
		
	</div>	
    
</header>

<style>

    .union {
        width: 100vw; 
        position: relative;
        display: flex;
        background-color: #AA1717;
        color: white;
        justify-content: center;
        padding-bottom: 3rem;
        padding-top: 3rem;
        overflow-x: hidden;
    }

    .orientation {
        flex-direction: row;
        width: 90%;
        display: flex;
        position: relative;
        justify-content: center;
        margin-right: -2.5vw;
    }

    .address {
        padding-right: 3vw;
    }

	header a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 2.5vw;
		color: white;
		font-size: 1.2rem;
		letter-spacing: 0.035em;
		text-decoration: none;
		transition: color 0.2s linear;
        font-style: normal;
        margin-top: -.7rem;
	}

    h4 {
        text-align: left;
       position: relative;
	   font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		margin: 0; 
		padding-bottom: .3rem; 
        font-size: 1.75rem;
    }

    h6 { 
        text-align: left;
       position: relative;
	   font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		margin: 0; 
		padding: 0; 
        font-size: 1.1rem;
        width: 50% 
    }

    a:hover {
		text-decoration: underline;
	}

    @media (max-width: 1048px) {
        .orientation {
            flex-direction: column;
            padding-left: calc(3vw + 2rem);
    }

    h4 { 
        width: 70%;
    }

    .address {
        padding-bottom: 2rem;
    }

    header a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 1rem 0;
		color: white;
		font-size: 1.2rem;
		letter-spacing: 0.035em;
		text-decoration: none;
		transition: color 0.2s linear;
        font-style: normal;
        
	}
       
	}
	
</style>
