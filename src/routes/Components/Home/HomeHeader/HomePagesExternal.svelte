<script>

    
    let HISTORYPIC = "https://axa-website-ink.s3.amazonaws.com/House+Picture093+copy.png"
    let ONCAMPUSPIC = "https://axa-website-ink.s3.amazonaws.com/beer+pong+top+copy.jpg"
    const pages = new Set([[ONCAMPUSPIC, 'On Campus', '/oncampus'], [HISTORYPIC, 'History', '/history']]);
	
</script>


<header>
	<link rel="stylesheet" href="https://use.typekit.net/dlr4khc.css">
	
	
	<div class="landing-info-outer">
		
        <div class="image-outer">
             {#each [...pages] as item}
                        <div class="image-inner" >
                            <a class="image-wrapper" href={item[2]} >
                                
                                <img src={item[0]} alt={item[1]}>

                                <div class="text-wrapper">
                                    <h2>
                                        {item[1]}
                                    </h2>
                                </div>
                            </a>
						</div>
			        {/each}
        </div>
       
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
        overflow-x: hidden;
	}

    .image-outer { 
        width: 100vw; 
        display: flex;
        align-items: center;
        flex-direction: row;
        position: relative;
         object-fit: contain;
    }

    .image-wrapper { 
         width: 50vw;
        height: 27rem;
        overflow: hidden;
        display: grid;
       text-align: center;
       position: relative;
       place-items: center;
       border-style: none;
       padding: 0;
       margin: 0
    
    }

    .image-wrapper img {
       width: 50vw;
        height: 27rem;
        opacity: .2;
        z-index: 0;
        filter: grayscale(100%);
       opacity: .2;
       object-fit: cover;
       transition: transform 1s;
    }


    .image-inner { 
        display: flex;
        align-items: center;
        flex-direction: column;
        position: relative;
        

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

     h2 {
        text-align: center;
       position: relative;
	   font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		margin: 0; 
		padding: 0; 
        font-size: calc(3rem + 2.5vw);
    }
    
    a {
        color: black;
        
    }

    a:hover {
        color: #AA1717
    }

    .image-wrapper img:hover {
       transform: scale(1.1);
    }

    @media (max-width: 660px) {
    .image-outer { 
       
        flex-direction: column;
        
    }
    .image-wrapper { 
         width: 100vw;
        height: 20rem;
        
    
    }

    .image-wrapper img {
       width: 100vw;
        height: 20rem;
       
    }
    
    }
	
</style>
