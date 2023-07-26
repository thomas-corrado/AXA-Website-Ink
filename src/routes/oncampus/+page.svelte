<svelte:head>
	<title>AXA | On Campus</title>
	<meta name="description" content="Alpha Chi Alpha On Campus" />
</svelte:head>

<script>
	import GeneralHeader from "../Components/GeneralHeader.svelte";
	import Accordion from "../Components/Accordion.svelte";
	import GenericUndergradGrid from "./GenericUndergradGrid.svelte";
	import GenericOfficerGrid from "./GenericOfficerGrid.svelte";

	const officer_array = [
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Evan Philips', 
			position: "President"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BrianZheng.jpg', 
			name: 'Brian Zheng', 
			position: "Vice President"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Colton Sankey', 
			position: "House Manager"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Ansh Patel', 
			position: "Treasurer"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BenTraugott.jpg', 
			name: 'Ben Traugott', 
			position: "Social Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Drew Barry', 
			position: "Social Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Ben Fagell', 
			position: "Social Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Andrew Doerr', 
			position: "Social Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Justin King', 
			position: "Programming Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Ethan Litmans', 
			position: "Service Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Jon Pazen/Jeff Liu/et al.', 
			position: "DEI Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Spencer Meek', 
			position: "Wellness Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Eric Richardson', 
			position: "Secretary"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'George Richards', 
			position: "Rush Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Alejo Rincon', 
			position: "Rush Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Jack Ranani', 
			position: "Rush Chair"
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/Placeholder.jpg', 
			name: 'Andrew Xu', 
			position: "Rush Chair"
		}, 
		
	];
	
	const twentythree_array = [
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BenHarris.jpg', 
			name: 'Ben Harris', 
			hometown: 'San Francisco, CA', 
			major: 'Film & Media Studies modified with History, Human-Centered Design', 
			bio: 'I love to draw & paint, ski, and make movies. Director of SHEBA Dance Troupe, First Year Trips Leader, and TA in the ENGS department.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/LucasBoebel.jpg',
			name: 'Lucas Boebel', 
			hometown: 'Onalaska, WI', 
			major: 'Computer Science', 
			bio: 'Big yoinker who enjoys splerging and yeefing on occasion. Houseman for a year. Best Bustache 2022 second runner up. Now doing software engineering.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/GriffinKozlow.jpg',
			name: 'Griffin Kozlow', 
			hometown: 'Detroit, MI', 
			major: 'QSS & Music', 
			bio: 'I graduated already and thus I’m not writing a bio. Chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe chafe. So stupid so stupid Thomas crayondo you are sooooo stinky -10000'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/JackPoss.jpg',
			name: 'Jack Poss', 
			hometown: 'Signal Mountain, TN', 
			major: 'Economics & Anthropology', 
			bio: 'I graduated recently (June 11th, 2023).'
		},
	];

	const twentyfour_array = [
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BenTraugott.jpg', 
			name: 'Ben Traugott', 
			hometown: 'Port Hope, ON', 
			major: 'Economics & Environmental Studies', 
			bio: 'I am involved with the Dickey Center, the Ledyard Canoe Club, the Dartmouth Cords, and have worked with the Dartmouth Center for Social Impact as well as done research for the Environmental Studies Department and Energy Justice Clinic. Looking to work in climate finance, environmental economics and policy post-grad. I also enjoy lounging.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BrianZheng.jpg', 
			name: 'Brian Zheng', 
			hometown: 'Naperville, IL', 
			major: 'Government modified (Politics, Philosophy, & Economics); ENVS + Spanish minors', 
			bio: 'On campus, I am an Army ROTC cadet, the president of the Dartmouth Cords a cappella group, and co-president of the Sexual Assault Peer Alliance.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/DeclanOScannlain.jpg', 
			name: "Declan O’Scannlain", 
			hometown: 'Portland, OR', 
			major: 'Physics & Chemistry', 
			bio: 'At Dartmouth, I am on the cross country and track and field teams. I also volunteer at the Upper Valley Haven. I am interested in pursuing medicine.'
		}, 
	];

	const twentyfive_array = [
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/MasonChilders.jpg', 
			name: 'Mason Childers', 
			hometown: 'Bloomington, IN', 
			major: 'Computer Science modified with Math', 
			bio: 'I run track. I like basketball. I like friends. I like nature. I like movies.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/ElliotAlberts.jpg', 
			name: 'Elliot Alberts', 
			hometown: 'Newton, MA', 
			major: 'Engineering Sciences & Economics', 
			bio: 'I enjoy spending time outdoors (climb, ski, bike, paddle, and combinations of these activities), building things, tickling the ivories, yeeefing while cooking, eating after yeeefing, and hope to have a positive impact on the environment through a career in business or engineering management.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/ConnorAllen.jpg', 
			name: 'Connor Allen', 
			hometown: 'Wilton, CT', 
			major: 'Economics, minor in Mathematical Finance & French', 
			bio: 'I love skiing, hiking, falling into Wikipedia rabbit holes, playing piano, binging French TV shows, and writing for The Dartmouth. Big fan of dad music, strategy games, shamelessly plot-twist-reliant movies, and friendship, among other fun things. I have been described as a "snob" and a "Francophile" (by myself).'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/JeremyGart.jpg', 
			name: 'Jeremy Gart', 
			hometown: 'Denver, CO', 
			major: 'Cognitive Science, minoring in Human-Centered Design & Spanish', 
			bio: "I'm an active member of Dartmouth Ski Patrol, The D, and Alpha Chi Alpha. I enjoy slow walks, good food, and 2x MVP, 1x FMVP and NBA Champion Nikola Jokic."
		}, 
	];

</script>

<section>
<div class="on-campus">

	<div class="oncampus-header">
		<GeneralHeader image_string="https://axa-website-ink.s3.amazonaws.com/AXA_ND2_copy.jpg" alt_text="Men standing on roof picture" header_text="On Campus" margin_top_val="15rem"/> 
	</div>

	<Accordion>
		<span slot="head">Officers</span>
		<div slot="details" class="grid-layout">
			<GenericOfficerGrid axa_class_year={officer_array}/> 
		</div>
	</Accordion>

	<div class="hr-line">
		<hr/> 
	</div>
	
	<Accordion >
		<span slot="head">Undergrads</span>
		<div slot="details" class="grid-layout">
		<h2>
			2023 
		</h2>

		<GenericUndergradGrid axa_class_year={twentythree_array}/> 
		
		
		<h2>
			2024 
		</h2>

		<GenericUndergradGrid axa_class_year={twentyfour_array}/> 
		<h2>
			2025
		</h2>

		<GenericUndergradGrid axa_class_year={twentyfive_array}/> 
		</div>
	</Accordion>

	<div class="hr-line">
		<hr/> 
	</div>

	<Accordion>
		<span slot="head">Service & Philanthropy</span>
		<div slot="details" class="grid-layout">
			
		<p>
			The brotherhood is quite active in the local community and in giving back to it. Many members of the house choose to spend their free time helping out residents of the Upper Valley through programs like DREAM and the Outdoor Leadership Experience. Others choose to contribute on either the national or global scale through involvement with the Tucker Center or through clubs like Dartmouth Coalition for Global Health.
		</p>
		<p>
			The house as a whole dedicates time and funding each term to support community service endeavors. Members have found that, despite their busy schedules, this is often some of the most important time they spend every term.


		</p>

		<p>
			During the ’17-’18 school year, Alpha Chi participated in/organized a number of service events, including a Halloween party for local kids from public housing in the area, meal prep for elderly in the Upper Valley, and a first-ever AXA Service Weekend, which included our yearly “Sausagefest” benefiting prostate cancer research. ”


		</p>
		<p>
			In the fall of 2016, the house won a campus-wide contest for CHaD participation, coming in with a substantially larger number of registered members than any other Greek house.


		</p>
		<p>
			Over the 2016 summer term, every brother on campus was involved with the Prouty, and together raised over $2000. The brotherhood also held a campus-wide volleyball tournament to benefit Action Against Hunger, and cooked meals for members of the local community with Students Fighting Hunger.


		</p>
		<p>
			In spring of 2016, the house participated in the Relay for Life, raising money to fight against cancer, and prepared dinners through Students Fighting Hunger.
		</p>
		</div>
	</Accordion>
</div>
</section>


<style>

	section {
		width: 100%;
		height: 100%;
		margin: 0;
		padding: 0;
		display: flex;
		font-family: "edita", serif;
		font-weight: 400;
		font-style: normal;
		display: flex;
		position: relative;
	}

	.on-campus { 
		width: 100%; 
		display: flex;
		flex-direction: column;
  		align-items: center;
  		justify-content: center;
		padding-bottom: 20px;
	}

	.oncampus-header { 
		padding-bottom: 20px;
	}

	.grid-layout {
		width: 90%;
		position: relative;
		justify-self: center;
		align-self: center;
	}

	h2 { 
		text-align: center;
		font-size: calc(2.25rem + 1vw);
		padding-top: 10px;
		padding-bottom: 25px;
		margin: 0;
	}

	.hr-line {
		width: 100vw;
		height: 100%;
		margin-top: 5px; 
		margin-bottom: 5px; 
		padding: 0;
		
	}

	.hr-line hr {
		
		display: flex;
		border-color: grey;
		border-width: .5px;
	}

	p {
		font-size: large;
	}
	

</style>
