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
			image_url: 'https://axa-website-ink.s3.amazonaws.com/EvanPhillips.jpg', 
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
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BenFagell.jpg', 
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
			image_url: 'https://axa-website-ink.s3.amazonaws.com/GeorgeRichards.jpg', 
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
			image_url: 'https://axa-website-ink.s3.amazonaws.com/AndrewXu.jpg', 
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
			bio: 'AXA Houseman for a year. Best Bustache 2022 second runner up. Now doing software engineering.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/GriffinKozlow.jpg',
			name: 'Griffin Kozlow', 
			hometown: 'Detroit, MI', 
			major: 'QSS & Music', 
			bio: 'I am involved in First-year trips, the Dartmouth music production community, and served as a social chair for Alpha Chi. I am now doing product and corporate strategy in LA.'
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
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/EvanPhillips.jpg', 
			name: "Evan Phillips", 
			hometown: 'Chapel Hill, NC', 
			major: 'Computer Science modified with Economics', 
			bio: 'Two truths and one lie about me: I was a recent First Team All-Lank 2023 selection, I dabble in ultimate frisbee and CS TAing, and I am Grammy award winning artist Macklemore.'
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/BenFagell.jpg', 
			name: "Ben Fagell", 
			hometown: 'Bethesda, MD', 
			major: 'Government Major, Middle Eastern Studies Minor', 
			bio: 'On campus, I am Managing Editor for the D, work with Dartmouth Consulting Group, and serve as social chair for AXA. I also performed research on immigration trends in the Gov department and travelled to London for the FSP at LSE. Oh, and I love poker.'
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
			bio: 'I enjoy spending time outdoors (climb, ski, bike, paddle, and combinations of these activities), building things, cooking, eating, and hope to have a positive impact on the environment through a career in business or engineering management.'
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
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/TommyCorrado.jpg', 
			name: 'Tommy Corrado', 
			hometown: 'Lancaster, PA', 
			major: 'Computer Science & History', 
			bio: "Here at Dartmouth, I am involved with The Dartmouth, the Dartmouth Admissions Office, and occasionally, the Book Arts Workshop. Outside of Dartmouth, I enjoy running outside, eating Go Go Squeezes, hammocking, reading, and live music, moviegoing, and exploring museums. I also engage in independent web development."
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/MattKoff.jpg', 
			name: 'Matt Koff', 
			hometown: 'Kensington, MD', 
			major: 'History', 
			bio: "On campus, I am involved with Ujima Dance Troupe, I am the Co-Chair of Outreach for SAPA, a member of Hanover Community Kitchen, a Tour Guide, and a member of Ledyard Canoe Club. I hope to pursue a career in law and Civil Rights advocacy. I love how I look and who I am on most if not all days. Other than that, I'm not quite sure who I am or what I'm doing here."
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/PabloPinedaPerez.jpg', 
			name: 'Pablo Pineda Perez', 
			hometown: 'Oberlin, OH', 
			major: 'Anthropology & Chemistry', 
			bio: "I am an Anthropology major and Chemistry minor. On campus I am involved in the Ledyard Canoe Club."
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/GeorgeRichards.jpg', 
			name: 'George Richards', 
			hometown: 'Minneapolis, MN', 
			major: 'Engineering Sciences & Economics', 
			bio: "I enjoy being outside, spending time with friends, listening to music, and building things. Outside of AXA, I'm involved in the Sports Analytics club, and I find myself being constantly disappointed by all Minnesota sports teams."
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/RyanTripp.jpg', 
			name: 'Ryan Tripp', 
			hometown: 'Piedmont, CA', 
			major: 'Environmental Engineering', 
			bio: "I'm on the lightweight rowing team and enjoy exploring nature in the upper valley and reading."
		}, 
		{
			image_url: 'https://axa-website-ink.s3.amazonaws.com/AndrewXu.jpg', 
			name: 'Andrew Xu', 
			hometown: 'Montville, NJ', 
			major: 'Quantitative Social Science', 
			bio: "I am currently majoring in Quantitative Social Science, and I am interested in pursuing consulting or finance. Outside of the classroom, I am enjoy skiing during the winters, and golfing every time else. I am also captain of the club tennis team. In terms of on-campus clubs I have been apart of, I am a member of DIPP and formerly on The Dartmouth Sales and Finance Team."
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
