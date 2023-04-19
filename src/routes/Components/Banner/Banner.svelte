<script>
	import IoIosMenu from 'svelte-icons/io/IoIosMenu.svelte'
	import MediaQuery from "../../MediaQuery.svelte"
	import { page } from '$app/stores';
	import { fly } from 'svelte/transition';
	

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
							<img src="src/lib/images/AXA-Logo-Red-New.png" alt='axa-logo'> 
						</div>
						<div class="letter-logo-wrapper">
							<img src="src/lib/images/LETTER-LOGO.png" alt='axa-logo'> 
						</div>
					</button>
				</a>
			{:else}
				<a class="logo-link" href="/">
					<button class="logo-button">
						<div class="mobile-logo-wrapper">
							<img src="src/lib/images/AXA-Logo-Red-New.png" alt='axa-logo'> 
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
	width: 7.5rem;
}

	header {
		width: 100%;
		justify-content: center;
		display: flex;
		background-color: #fff;
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
		
		padding-left: .5rem;
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
  background-color: white; 
  /* position: relative;
  flex-direction: column;
  display: flex;
  width: auto; */
  
}

/* Hide the links inside the navigation menu (except for logo/home) */
.topnav #my-links {
  display: block;
   
}

/* Style navigation menu links */
.topnav a {
  color: #C02126;
  padding: 14px; 
  /* padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
  display: block;
  text-align: right; */
}
</style>
