<script>

    let HOUSEPIC = "https://axa-website-ink.s3.us-east-1.amazonaws.com/IMG_9765.JPG?response-content-disposition=inline&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEIb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMiJGMEQCIHLuwUkWzcP8lUT%2BNZoaxSiLNcPFfmbEcwgLGGppIcabAiA2eS%2BPD9GpFxKybVCq6VzsN3b2gODyDF8AjRImg%2FWGcCrkAgh%2FEAAaDDg4NDEzMDQ1OTUyNiIMni6O1geTiJe0hlaBKsEC%2BhfYqQOwpvn2tUGGFD0Oud5OBFjCzsmdsPeGYi4HGXoYBODToN5C1xKwsYF3%2BW3Lug1xXmM090eo9SICASAWzfgOixsLJVoKNy5NQ8wJmNYNQrcJJukyR3kamNx8fYxVhyaqHATc6hPZgvZrSQJet19kKoqYiqJSomOI%2FYKVgCSoF68%2BXrxa0%2FiUeAvw6oGLJ7zkPc2yJv2euwI7xMs%2FJTUk6sNpJPVr4aZV6VFWGsSNPeluHZJZ6iQsk7wnCGLap4DNYR3FX8TuLnaf9cUn1babue31U8rdCDKMlCYBZ3%2FTyoU0aPgjA2nYdaFEkIwxn1VsEEw6iE%2BKSMIwrsgvEWECPVYvemQhJpgEUg0KHS204ailHNwJkmSKc1WM0G%2BvcrQzeJB0XusGt70KHOb3UXf6xbXarbOYK5TyC%2FtaSI7SMLnDgaIGOrQCnzbLjsjKnFi%2FmIHzq%2BFXF9TJhN3BVbN8fVAo5ISMmhXfmGygpIFG5kxmB0oBDnORxtPrkzUjwTHdYoXcheSD5s5MVdnjIwPo05Il3J5Ulh8fcjjbpoU87KwfvRwBQWstF4FgjiRPwyO1VCrOIez089l4yO%2BYSbABGWRA7vJ4aJoS%2BQChAMk6H5yRpgXGMD0E3Xbkeeoqd8BLHGwxnNrinaZhreFLPjHt%2B%2BcLafTQ5p4ti2F5cuKDu5A6FikRPKYzH9B%2BVFpS8bRWL9zy5ex2hdABhisU9LbKpzOShaYhLS2suy9RNkKy399KgqxW5gmeWgHMcD%2ByduAbz0wnY74%2BDD%2FRRuyacyF30eXW9c1Vnk%2B4ETLSxhtXJGt99BSzI1u6qCq58HnxWxN2DLioZnmfnYOLAsA%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230419T215642Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIA43WSIF6DEUEMDKBE%2F20230419%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=70dc2d60074c6ec952f8273113400a494c44936a7ec0800d2e2aa0cd2753fcea"
	
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
