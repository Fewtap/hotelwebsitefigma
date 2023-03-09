<script lang="ts">
	import { onMount } from 'svelte';
	let rightcolumnheight: number = 0;

	onMount(() => {
		//if the width of the screen is over 1000px
		if (window.innerWidth > 1000) {
			handleScroll();
		}

		//on window resize
		window.addEventListener('resize', () => {
			if (window.innerWidth > 1025) {
				handleScroll();
			} else {
				let cards = document.querySelectorAll('.card');
				cards.forEach((card) => {
					card.classList.remove('hide');
					card.classList.remove('show');
					card.style.opacity = '1';
					card.style.transform = 'scale(1)';
				});
			}
		});
	});

	function handleScroll() {
		const rightColumn = document.getElementById('right-column');
		const cards = document.querySelectorAll('.card');
		const rightColumnHeight = rightColumn.clientHeight;
		const rightcolumncenter = rightColumnHeight / 2 + rightColumnHeight;

		const rightColumnTop = rightColumn.getBoundingClientRect().top;

		cards.forEach((card) => {
			const cardRect = card.getBoundingClientRect();
			const cardTop = cardRect.top - rightColumnTop;
			const cardBottom = cardRect.bottom - rightColumnTop;
			const cardMiddle = (cardTop + cardBottom) / 2;

			// Calculate the opacity based on the card's position relative to the middle of the right column
			let value = 1 - (cardMiddle / rightcolumncenter) * 2 + 0.4;

			if (value < 0) value = 0;

			//set the opacity and the scale of the card
			if (value > 0.5) {
				card.classList.remove('hide');
				card.classList.add('show');
			} else {
				card.classList.add('hide');
				card.classList.remove('show');
				card.style.opacity = value.toString();
				card.style.transform = `scale(${value})`;
			}

			if (value > 1) {
				card.classList.add('hide');
				card.classList.remove('show');
				//if the value is 1.2 set the opacity to 0.8 and so on
				card.style.opacity = (2 - value).toString();
				card.style.transform = `scale(${2 - value})`;
				if (card === cards[cards.length - 1] && value > 0.5) {
				}

				//
			}

			if (card === cards[cards.length - 1] && value > 0.5) {
				card.classList.remove('hide');
				card.classList.add('show');
			}
		});
	}
</script>

<div class="outercontainer">
	<div class="container">
		<div class="left-column">
			<h2>VÆRELSER</h2>
			<p>
				Best Western Plus Hotel Ilulissat har 78 moderne værelser fordelt på 5 forskellige
				værelsestyper - 30 standardværelser, 12 familieværelser, 18 executive værelser, 16 superior
				værelser og 2 suiter. Det er derfor et af Grønlands største hoteller!
			</p>

			<h4>
				<br />Alle værelser har privat bad og toilet, dobbeltsenge, samt nedenstående faciliteter:
			</h4>
			<ul>
				<li>Gratis trådløst internet</li>
				<li>Fladskærmsfjernsyn</li>
				<li>Chrome Cast</li>
				<li>Skrivebord</li>
				<li>Gæstfrihedsbakke med elkedel</li>
				<li>Kaffe og te</li>
				<li>Ekstra hovedpude</li>
				<li>Pengeskab</li>
				<li>Hårtørrer</li>
				<li>Babyseng ved henvendelse</li>
				<li>Strygeservice ved henvendelse i receptionen</li>
				<li>Toiletartikler, herunder shampoo, body lotion og sæbe</li>
				<li>Morgenkåbe og sutsko ved henvendelse</li>
			</ul>
		</div>
		<div
			class="right-column"
			bind:offsetHeight={rightcolumnheight}
			on:scroll={handleScroll}
			id="right-column"
		>
			<div class="card">
				<img
					src="https://static.wixstatic.com/media/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg"
					alt="Placeholder Image"
				/>
				<div class="card-content">
					<h3>STANDARD VÆRELSE</h3>
					<p>
						Alle standardværelser har dobbeltsenge (2x90 cm) og moderne indretning. Der er privat
						badeværelse med hovedbruser og toiletartikler, som shampoo, body lotion og sæbe.
						Hårtørreren vil være under håndvasken i badeværelset. Udsigten fra værelset vil være ud
						over Ilulissat by og dens omliggende smukke natur. Størrelse: 14,7 kvm
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
						primært af Ilulissat by med Ilulissat Isfjord og Diskobugten i baggrunden. Størrelse:
						21,1 kvm
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
						Det ene værelse er et soveværelse med seng og garderobe. Det andet værelse er en stue,
						og denne har en sofa, lille spisebord, samt et mindre tekøkken. Størrelse: 43 kvm
					</p>
				</div>
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	$accent: #003c7e;
	$primary: #f1e1ce;

	@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
	:global(.show) {
		transform: scale(1) !important;
		opacity: 1 !important;
		transition: cubic-bezier(0.68, 0.1, 0.265, 1) 0.3s;
	}

	:global(.hide) {
		transition: ease 0.3s;
	}

	.outercontainer {
		background-repeat: no-repeat;
		background-size: cover;
		height: 100vh;

		background: url('https://images.wallpaperscraft.com/image/single/whale_tail_ocean_123547_2560x1440.jpg');
	}

	h1,
	h2,
	h3,
	h4,
	h5,
	h6,
	p,
	ul,
	li,
	span,
	div,
	button,
	a {
		color: white;
		font-family: 'Oswald', sans-serif;
	}

	p {
		font-size: 1em;
	}

	h4 {
		font-size: 1.2em;
		font-weight: 900;
	}

	ul {
		padding: 0;
		font-size: 0.9em;
		text-align: left;
	}

	h2 {
		text-align: center;
		color: $primary;
		font-weight: 700;
	}

	h3 {
		color: $primary;
		font-weight: 400;
	}

	div {
		box-sizing: border-box;
	}

	.container {
		display: flex;
		align-items: center;
		justify-content: space-around;
		overflow-y: hidden;
	}

	.left-column {
		width: 30%;
		background-color: $accent;
		height: 70%;
		border-radius: 20px;
		margin: 50px;
		padding: 100px;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.right-column {
		padding: 15% 0px 25% 0px;
		height: 100vh;
		/*make the div scrollable but hide the scrollbar*/

		/*center the content without flexbox*/
		margin: auto auto;

		overflow-y: scroll;
		width: 50%;

		margin: 20px;
		background-color: transparent;

		& p {
			font-size: 0.8em;
		}
	}

	.right-column::-webkit-scrollbar {
		display: none;
	}

	.card {
		background-color: $accent;
		height: 500px;
		width: 100%;
		display: flex;
		align-items: center;
		margin-inline: auto;
		border-radius: 20px;

		/*add margin to the bottom of the card*/
		margin-bottom: 20px;
	}

	.card img {
		max-width: 60%;
		height: 100%;
		/*make the image have the same border radius as the card*/
		border-radius: 20px 0 0 20px;
	}

	.card-content {
		margin-inline: 20px;
		font-size: 1.3em;
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
	@media screen and (min-width: 1000px) {
		:global(body) {
			background-repeat: no-repeat;
		}

		.container {
			height: 100vh;
		}
	}

	@media screen and (max-width: 768px) {
		.container {
			flex-direction: column;
			padding-inline: 20px;
			background: url('https://images.wallpaperscraft.com/image/single/whale_tail_ocean_123547_2560x1440.jpg');
		}

		.left-column {
			width: 100%;
			margin: 20px;
			padding: 50px;
			margin-top: 5em;
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
			min-width: 100%;
			height: auto;
			border-radius: 20px 20px 0 0;
		}

		.card-content {
			margin: 20px;
		}
	}

	@media screen and (min-width: 768px) and (max-width: 1000px) {
		.container {
			flex-direction: row;
			flex-wrap: wrap;
			justify-content: space-evenly;
			background: url('https://images.wallpaperscraft.com/image/single/whale_tail_ocean_123547_2560x1440.jpg');
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

	@media screen and (min-width: 1200px) {
		.container {
			overflow: hidden;
		}
		li {
			font-size: 0.9em;
		}

		p {
			font-size: 0.9em;
		}
	}
</style>
