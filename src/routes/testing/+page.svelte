<script lang="ts">
	import { onMount } from 'svelte';
	let rightcolumnheight: number = 0;

	onMount(() => {
		let card = document.querySelectorAll('.card')[0];
		let column = document.getElementById('right-column');
		column?.scrollTo(card);
	});

	function handleScroll() {
		let rightcolumn = document.getElementById('right-column');
		let cards = document.querySelectorAll('.card');

		//get the card closest to the middle of the right column
		console.log('scrolling');

		cards.forEach((element) => {
			let bottom = element.getBoundingClientRect().bottom;
			let top = element.getBoundingClientRect().top;

			//get the opacity of the card based on how far it is from the top of the right column
			let opacity = 1 - (top / rightcolumnheight) * 2;

			opacity += 0.5;

			element.style.opacity = opacity.toString();
		});
	}
</script>

<div class="container">
	<div
		class="right-column"
		bind:offsetHeight={rightcolumnheight}
		on:scroll={handleScroll}
		id="right-column"
	>
		<div class="card">
			<img
				src="https://static.wixstatic.com/media/ca17e2_e28aa910ae9145d6872ee0a78958d0a9~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_e28aa910ae9145d6872ee0a78958d0a9~mv2.jpg"
				alt="Placeholder Image"
				class="card-image"
			/>
			<div class="card-content">
				<h3>SUPERIOR VÆRELSE</h3>
				<p>
					Samtlige superiorværelser har dobbeltsenge (2x90 cm). Udsigten fra værelset vil være ud
					over Ilulissat Isfjord og Diskobugten. Størrelse: 21,1 kvm
				</p>
			</div>
		</div>
		<div class="card">
			<img
				src="https://static.wixstatic.com/media/ca17e2_5819dd786e5b4abb8e973aa5ce497757~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_5819dd786e5b4abb8e973aa5ce497757~mv2.jpg"
				alt="Placeholder Image"
			/>
			<div class="card-content">
				<h3>FAMILIE VÆRELSE</h3>
				<p>
					Alle familieværelser har dobbeltsenge (2x90 cm) og to foldud-senge, så en familie, der
					består af to voksne og to børn nemt kan bo på disse værelser. Udsigten fra værelset er
					primært af Ilulissat by med Ilulissat Isfjord og Diskobugten i baggrunden. Størrelse: 21,1
					kvm
				</p>
			</div>
		</div>
		<div class="card">
			<img
				src="https://static.wixstatic.com/media/ca17e2_e28aa910ae9145d6872ee0a78958d0a9~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_e28aa910ae9145d6872ee0a78958d0a9~mv2.jpg"
				alt="Placeholder Image"
			/>
			<div class="card-content">
				<h3>SUPERIOR VÆRELSE</h3>
				<p>
					Samtlige superiorværelser har dobbeltsenge (2x90 cm). Udsigten fra værelset vil være ud
					over Ilulissat Isfjord og Diskobugten. Størrelse: 21,1 kvm
				</p>
			</div>
		</div>
		<div class="card">
			<img
				src="https://static.wixstatic.com/media/ca17e2_e203e05823274989b7463e12bda87ca9~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_e203e05823274989b7463e12bda87ca9~mv2.jpg"
				alt="Placeholder Image"
			/>
			<div class="card-content">
				<h3>EXECUTIVE VÆRELSE</h3>
				<p>
					Alle executiveværelser har dobbeltsenge (2x90 cm). Udsigten fra værelset er ud over
					Ilulissat Isfjord og Diskobugten. Der er to størrelser af executiveværelserne: 18,6
					kvadratmeter og 20,5 kvadratmeter. Forskellen på disse to er placeringen.
				</p>
			</div>
		</div>
		<div class="card">
			<img
				src="https://static.wixstatic.com/media/ca17e2_2e9c4806c8834515883de4dc6e20d4f6~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_2e9c4806c8834515883de4dc6e20d4f6~mv2.jpg"
				alt="Placeholder Image"
			/>
			<div class="card-content">
				<h3>SUITE</h3>
				<p>
					Vores suiter er placeret på 5. etage med bjergtagende udsigt og inkluderer to værelser.
					Det ene værelse er et soveværelse med seng og garderobe. Det andet værelse er en stue, og
					denne har en sofa, lille spisebord, samt et mindre tekøkken. Størrelse: 43 kvm
				</p>
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.a {
		background: red;
	}

	ul {
		padding: 0;
	}

	h2 {
		text-align: center;
	}

	h3 {
		color: crimson;
		font-weight: 900;
		font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
	}

	div {
		box-sizing: border-box;
	}

	.container {
		display: flex;
		align-items: center;
		justify-content: space-around;
		background-repeat: no-repeat;
		background-size: cover;
		background: url('https://static.wixstatic.com/media/nsplsh_65324d6e4b6c4546635467~mv2_d_7360_4912_s_4_2.jpg/v1/fill/w_2543,h_1556,al_t,q_90,usm_0.66_1.00_0.01,enc_auto/nsplsh_65324d6e4b6c4546635467~mv2_d_7360_4912_s_4_2.jpg');
	}

	.left-column {
		width: 30%;
		background-color: #f1f1f1;
		height: fit-content;
		border-radius: 20px;
		margin: 50px;
		padding: 100px;
	}

	.right-column {
		padding-top: 5%;
		height: 1080px;
		/*make the div scrollable but hide the scrollbar*/

		/*center the content without flexbox*/
		margin: auto auto;

		overflow-y: scroll;
		width: 50%;
		background-color: #f1f1f1;
		margin: 20px;
		background-color: transparent;
	}

	.right-column::-webkit-scrollbar {
		display: none;
	}

	.card {
		background-color: transparent;
		position: relative;
		cursor: pointer;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.card-image {
		width: 100%;
		border-radius: 20px 20px 0 0;
		transition: all 0.3s ease-in-out;
		/*add a border to the bottom of the image*/
		border-bottom: 1px solid #f1f1f1;
	}

	.card:hover .card-image {
		opacity: 0.7;
	}

	.card-content {
		background-color: #f1f1f1;
		border-radius: 0 0 20px 20px;
		width: 100%;
		padding: 20px;
		display: block;
		transform: scaleY(0);
		transform-origin: top;
		font-size: 1.3em;
		transition: all 0.3s ease-in-out;
		animation: bounce 1s ease-in-out infinite;
		animation-delay: 500ms;
	}

	.card:hover .card-content {
		transform: scaleY(1);
		transition: cubic-bezier(0.33, 1.03, 0.76, 1.27) 0.3s;
		transform-origin: top;
	}

	@media screen and (max-width: 1400px) {
		.right-column {
			font-size: 0.5em;
		}
		.left-column {
			font-size: 1.1em;
			padding: 3em;
		}
	}

	/*media query for desktops*/
	@media screen and (min-width: 1024px) {
		:global(body) {
			background: url('https://static.wixstatic.com/media/nsplsh_65324d6e4b6c4546635467~mv2_d_7360_4912_s_4_2.jpg/v1/fill/w_2543,h_1556,al_t,q_90,usm_0.66_1.00_0.01,enc_auto/nsplsh_65324d6e4b6c4546635467~mv2_d_7360_4912_s_4_2.jpg');
		}

		.container {
			height: 100vh;
		}
	}

	@media screen and (max-width: 768px) {
		.container {
			flex-direction: column;
			padding-inline: 20px;
		}

		.left-column {
			width: 100%;
			margin: 20px;
			padding: 50px;
		}

		.right-column {
			width: 100%;
			/*add a margin to the sides of the div*/
			margin-inline: 20px;
			height: auto;
			overflow-y: visible;
		}

		.card {
			height: auto;
			flex-direction: column;
		}

		.card img {
			width: 100%;
			height: auto;
			border-radius: 20px 20px 0 0;
		}

		.card-content {
			margin: 20px;
		}
	}

	@media screen and (min-width: 768px) and (max-width: 1024px) {
		.container {
			flex-direction: row;
			flex-wrap: wrap;
			justify-content: space-evenly;
		}

		.left-column {
			width: fit-content;
			padding: 5%;
		}

		.right-column {
			width: 60%;
			margin: 20px;
			height: auto;
			overflow-y: visible;
		}

		.card {
			height: auto;
			flex-direction: column;
		}

		.card img {
			min-width: 100%;
			border-radius: 20px 20px 0 0;
		}

		.card-content {
			margin: 20px;
			font-size: 2em;
			padding: 20px;
		}
	}
</style>
