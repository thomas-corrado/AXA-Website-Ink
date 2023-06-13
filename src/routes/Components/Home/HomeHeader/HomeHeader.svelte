<script>

    let HOUSEPIC = "https://axa-website-ink.s3.amazonaws.com/IMG_9765.JPG"
	
</script>


<header>
	<link rel="stylesheet" href="https://use.typekit.net/dlr4khc.css">
	
	
	<div class="home-header">
         
        <div class="image-wrapper">
            <img src={HOUSEPIC} alt='axa-2023-house'>
            
            <div class="text-wrapper">
                <h1>
                Welcome to Alpha Chi Alpha
            </h1>
            <h2>
                Fidelis et Suavis
            </h2>
            </div>
            
        </div>

        
		
	</div>	
</header>

<style>
    .home-header {
        width: 100%; 
        position: relative;
       
    }   

    .image-wrapper { 
         width: 100vw;
        height: calc(70vh - 5vw);
        overflow: hidden;
        display: grid;
       text-align: center;
       position: relative;
       place-items: center;
       
       
    }

    .image-wrapper img {
        min-width: 100%;
        min-height: 100%;
        width: auto;
        height: auto;
        opacity: .3;
        z-index: 0;
        
    }

    .text-wrapper {
        width: 80%;
        opacity: 1;
        z-index: 1;
        padding: 0;
        margin: 0;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .text-wrapper h1 {
         font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		color: black;
        font-size: 10vh;
        opacity: 1;
        z-index: 1;
        padding: 0;
        margin: 0;
        align-items: center;
    }

    .text-wrapper h2 {
         font-family: "edita", serif;
		font-weight: 400;
		font-style: italic;
		color: black;
        font-size: 10vh;
        opacity: 1;
         z-index: 1;
         padding: 0;
        margin: 0;
    }

    @media (max-width: 665px) {
        .text-wrapper {
        width: 80%;
        
    }
        .text-wrapper h1 {
   
        font-size: calc(6vh + 2vw);
 
    }
		.text-wrapper h2 {
   
        font-size: calc(6vh + 2vw);
 
    }
	}

    

    
	
</style>
