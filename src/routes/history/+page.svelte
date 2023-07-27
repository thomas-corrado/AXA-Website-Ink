<svelte:head>
	<title>AXA | History</title>
	<meta name="description" content="Alpha Chi Alpha History" />
</svelte:head>

<script>
	import GeneralHeader from "../Components/GeneralHeader.svelte";

</script>

<section>
<div class="History">
	<div>
		<GeneralHeader image_string="https://axa-website-ink.s3.amazonaws.com/sketch_house_copy.jpg" alt_text="house sketch of Alpha Chi Alpha house" header_text="History" margin_top_val="15rem"/> 
	</div>

	<div class="HeaderText">
		<p>
			In 1916, six undergraduates joined together in the name of loyalty and brotherhood and founded the fraternity that is now Alpha Chi. At first an informal debating group, they met under the guidance of Dr. Henry Wells Lawrence, Jr., a professor of History at the College. As the meetings became more regular, these undergraduates organized themselves into a fraternity they called The Ledyard Club, with the ultimate goal of securing a charter from the national Alpha Chi Rho, of which Dr. Lawrence had been a founding member at Yale.
		</p>

		<p>
			Toward that goal, The Ledyard Club reorganized themselves as Epsilon Kappa Alpha and increased their membership to twelve men. Their physical plant was located behind the old white church on the north side of campus. Three years later, EKA joined the national fraternity Alpha Chi Rho and became their Phi Nu chapter. In 1936, the Depression led the Phi Nu's to merge with Phi Kappa Sigma forming Gamma Delta Chi. They existed as part of Gamma Delt until 1959 when the Phi Nu chapter of Alpha Chi Rho re-emerged. Nine Gamma Delts separated from the fraternity in an effort to rediscover the sense of brotherhood that had disappeared with the large pledge classes of the 1950s. It was at this point that they moved into the house on Webster Avenue which currently houses Alpha Chi.
		</p>
		
		<p>
			Conflicts soon developed between the ideals of Phi Nu and those of the national house. In 1963, after being forced to participate in mystical ceremonies which Phi Nu found to be inappropriate at a college of liberal learning, the fraternity went local. They replaced the Rho with an Alpha, signifying a new beginning and became Alpha Chi Alpha, the local house we know today.
		</p>
	</div>

	
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
		color: black;
		
	}

	.History { 
		width: 100%; 
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0;
		padding: 0;
	}

	p {
		font-size: large;
	}

	.HeaderText {
		padding-top: 20px;
		padding-bottom: 20px;
		width: 80%;
		text-align: center;
	}

</style>
