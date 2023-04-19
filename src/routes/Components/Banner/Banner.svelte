<script>
	import IoIosMenu from 'svelte-icons/io/IoIosMenu.svelte'
	import MediaQuery from "../../MediaQuery.svelte"
	import { page } from '$app/stores';
	import { fly } from 'svelte/transition';

	let AXALogoRedNew = "https://axa-website-ink.s3.us-east-1.amazonaws.com/AXA-Logo-Red-New.png?response-content-disposition=inline&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEIb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMiJGMEQCIHLuwUkWzcP8lUT%2BNZoaxSiLNcPFfmbEcwgLGGppIcabAiA2eS%2BPD9GpFxKybVCq6VzsN3b2gODyDF8AjRImg%2FWGcCrkAgh%2FEAAaDDg4NDEzMDQ1OTUyNiIMni6O1geTiJe0hlaBKsEC%2BhfYqQOwpvn2tUGGFD0Oud5OBFjCzsmdsPeGYi4HGXoYBODToN5C1xKwsYF3%2BW3Lug1xXmM090eo9SICASAWzfgOixsLJVoKNy5NQ8wJmNYNQrcJJukyR3kamNx8fYxVhyaqHATc6hPZgvZrSQJet19kKoqYiqJSomOI%2FYKVgCSoF68%2BXrxa0%2FiUeAvw6oGLJ7zkPc2yJv2euwI7xMs%2FJTUk6sNpJPVr4aZV6VFWGsSNPeluHZJZ6iQsk7wnCGLap4DNYR3FX8TuLnaf9cUn1babue31U8rdCDKMlCYBZ3%2FTyoU0aPgjA2nYdaFEkIwxn1VsEEw6iE%2BKSMIwrsgvEWECPVYvemQhJpgEUg0KHS204ailHNwJkmSKc1WM0G%2BvcrQzeJB0XusGt70KHOb3UXf6xbXarbOYK5TyC%2FtaSI7SMLnDgaIGOrQCnzbLjsjKnFi%2FmIHzq%2BFXF9TJhN3BVbN8fVAo5ISMmhXfmGygpIFG5kxmB0oBDnORxtPrkzUjwTHdYoXcheSD5s5MVdnjIwPo05Il3J5Ulh8fcjjbpoU87KwfvRwBQWstF4FgjiRPwyO1VCrOIez089l4yO%2BYSbABGWRA7vJ4aJoS%2BQChAMk6H5yRpgXGMD0E3Xbkeeoqd8BLHGwxnNrinaZhreFLPjHt%2B%2BcLafTQ5p4ti2F5cuKDu5A6FikRPKYzH9B%2BVFpS8bRWL9zy5ex2hdABhisU9LbKpzOShaYhLS2suy9RNkKy399KgqxW5gmeWgHMcD%2ByduAbz0wnY74%2BDD%2FRRuyacyF30eXW9c1Vnk%2B4ETLSxhtXJGt99BSzI1u6qCq58HnxWxN2DLioZnmfnYOLAsA%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230419T215250Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIA43WSIF6DEUEMDKBE%2F20230419%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=b75f815d588a55c54bdb2fa81fc4c8816277d6f1854cdcec6810383ed4d5af2c"
	let LETTERLOGO = "https://axa-website-ink.s3.us-east-1.amazonaws.com/LETTER-LOGO.png?response-content-disposition=inline&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEIb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMiJGMEQCIHLuwUkWzcP8lUT%2BNZoaxSiLNcPFfmbEcwgLGGppIcabAiA2eS%2BPD9GpFxKybVCq6VzsN3b2gODyDF8AjRImg%2FWGcCrkAgh%2FEAAaDDg4NDEzMDQ1OTUyNiIMni6O1geTiJe0hlaBKsEC%2BhfYqQOwpvn2tUGGFD0Oud5OBFjCzsmdsPeGYi4HGXoYBODToN5C1xKwsYF3%2BW3Lug1xXmM090eo9SICASAWzfgOixsLJVoKNy5NQ8wJmNYNQrcJJukyR3kamNx8fYxVhyaqHATc6hPZgvZrSQJet19kKoqYiqJSomOI%2FYKVgCSoF68%2BXrxa0%2FiUeAvw6oGLJ7zkPc2yJv2euwI7xMs%2FJTUk6sNpJPVr4aZV6VFWGsSNPeluHZJZ6iQsk7wnCGLap4DNYR3FX8TuLnaf9cUn1babue31U8rdCDKMlCYBZ3%2FTyoU0aPgjA2nYdaFEkIwxn1VsEEw6iE%2BKSMIwrsgvEWECPVYvemQhJpgEUg0KHS204ailHNwJkmSKc1WM0G%2BvcrQzeJB0XusGt70KHOb3UXf6xbXarbOYK5TyC%2FtaSI7SMLnDgaIGOrQCnzbLjsjKnFi%2FmIHzq%2BFXF9TJhN3BVbN8fVAo5ISMmhXfmGygpIFG5kxmB0oBDnORxtPrkzUjwTHdYoXcheSD5s5MVdnjIwPo05Il3J5Ulh8fcjjbpoU87KwfvRwBQWstF4FgjiRPwyO1VCrOIez089l4yO%2BYSbABGWRA7vJ4aJoS%2BQChAMk6H5yRpgXGMD0E3Xbkeeoqd8BLHGwxnNrinaZhreFLPjHt%2B%2BcLafTQ5p4ti2F5cuKDu5A6FikRPKYzH9B%2BVFpS8bRWL9zy5ex2hdABhisU9LbKpzOShaYhLS2suy9RNkKy399KgqxW5gmeWgHMcD%2ByduAbz0wnY74%2BDD%2FRRuyacyF30eXW9c1Vnk%2B4ETLSxhtXJGt99BSzI1u6qCq58HnxWxN2DLioZnmfnYOLAsA%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230419T215418Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIA43WSIF6DEUEMDKBE%2F20230419%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=9353d32fe02bef24112c480f410c449c3e63711d41f26be8d9b3f7498402ee3e"
	 
	import {clickOutside} from './clickOutside';
	
	const pages = new Set([['ON CAMPUS', 'oncampus'], ['HISTORY', 'history'], ['ALUMNI', 'alumni'],['CONTACT', 'contact'], ['DONATE', 'donate']]);
	let open = false; 

	function handleClickOutside() {
		open = !open
	}
</script>


<header>
	<link rel="stylesheet" href="https://use.typekit.net/dlr4khc.css">
	
	
	<div class="union">

		<!-- Mobile Banner with Hamburger -->
		<MediaQuery query="(min-width: 590px)" let:matches>
			{#if matches}
				<a class="logo-link" href="/">
					<button class="logo-button">
						<div class="desktop-logo-wrapper">
							<img src={AXALogoRedNew} alt='axa-logo'> 
						</div>
						<div class="letter-logo-wrapper">
							<img src={LETTERLOGO} alt='axa-logo'> 
						</div>
					</button>
				</a>
			{:else}
				<a class="logo-link" href="/">
					<button class="logo-button">
						<div class="mobile-logo-wrapper">
							<img src={AXALogoRedNew} alt='axa-logo'> 
						</div>
					</button>
				</a>
			{/if}
		</MediaQuery>
		
		<!-- Desktop Banner without Hamburger -->
		<MediaQuery query="(min-width: 1145px)" let:matches>
			{#if matches}
				<ul>
					{#each [...pages] as item}
						<li>
							<a aria-current={$page.url.pathname === `/${item[1] !== '' ? item[1] : ''}` ? 'page' : undefined} href='/{item[1] !== '' ? item[1] : ''}'>{item[0]}</a>
						</li>
					{/each}
					
				</ul>
			{/if}
		</MediaQuery>

		<!-- Desktop Banner with Hamburger -->
		<MediaQuery query="(max-width: 1144px)" let:matches>
			{#if matches}

			{#if open}
				<nav class="topnav" use:clickOutside on:click_outside={handleClickOutside} transition:fly={{ x: 300, duration: 500}}>
					<div id="my-links" >
						{#each [...pages] as item}
							<a on:click={() => open=!open} class={item[1]} href='/{item[1] !== 'home' ? item[1] : ''}' aria-current={$page.url.pathname === `/${item[1] !== 'home' ? item[1] : ''}` ? 'page' : undefined} >{item[0]}</a>
						{/each}
					</div>
			</nav>
			
			{/if}
			
			<div class='inner-header'>
				<button on:click={() => open=!open}>
					{#if !open }
						<div class='icon' aria-label="menu-icon">
							<IoIosMenu />
						</div>		
					
					{/if}
				</button>
			</div>
			{/if}
		</MediaQuery>
	</div>	
</header>

<style>
	nav {
  position: fixed;
  top: 0;
  right: 0;
  height: 100%;
  padding: 2rem 1rem 0.6rem;
  
  background: #fff;
  overflow-y: auto;
	width: calc((13vw - 20rem) + 24rem);
	justify-content: center;
	z-index: 2;
}

	header {
		width: 100%;
		justify-content: center;
		display: flex;
		background-color: #fff;
		padding-bottom: 8px;
	}

	.inner-header {
		justify-content: right;
        background-color: white;
		display: flex;
		align-items: right;
		justify-items: right;
		width: 100%;
	}

	.union {
		display: flex;
		font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		color: #C02126;
		align-items: center;
		width: 97%;
		align-items: center;
		justify-items: center;
	}

	.logo-link {
		padding: 0;
		margin: 0;
	}

	.logo-button {
		display: flex;
		align-items: center;
		padding: 0;
		margin: 0;
		background-color: transparent;
		border: 0;
		
	}
	.desktop-logo-wrapper img {
		
		
		height: 9rem;
		
	}

	.mobile-logo-wrapper img {
		padding-left: .25rem;
		height: 5.5rem;
	}

	.letter-logo-wrapper img {
		width: 20rem; 
		padding-left: 1rem;
		
	}

	button {
		justify-content: flex-end;
		background-color: transparent;
		border: none;
		padding: 0;
	}


	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: right;
		width: 97vw;
		list-style: none;
		background: var(--background);
		background-size: contain;
		margin-right: -.5rem;
	}

	a[aria-current='page']{
	
		text-decoration: underline;
	}

	li {
		position: relative;
		height: 100%;
	}

	header a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1rem;
		color: var(--color-text);
		font-size: 1.2rem;
		letter-spacing: 0.035em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}

	.icon {
		color: #C02126;
		padding: 5px;
		width: 2rem;
	}

	.topnav {
  
  justify-content: center;
  /* position: relative;
  flex-direction: column;
  display: flex;
  width: auto; */
  text-align: center;
  
}

/* Hide the links inside the navigation menu (except for logo/home) */
.topnav #my-links {
 text-align: center;
   justify-content: center;
}

/* Style navigation menu links */
.topnav a {
  color: #C02126;
  padding: 14px; 
  text-align: center;
  justify-content: center;
  /* padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
  display: block;
  text-align: right; */
}
</style>
