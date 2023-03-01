<div class="maincontainer" id="cardscontainer">
	<div class="grid">
		<div class="pagetitle">
			<h1>Faciliteter</h1>
		</div>
		<div class="card">
			<div class="titlecontainer">
				<h2>Værelser</h2>
			</div>
			<div class="descriptioncontainer">
				<p>
					Oplev ultimativ komfort og afslapning på Hotel Ilulissats værelser. Vores værelser er
					designet til at give dig den perfekte kombination af moderne faciliteter og hyggelig
					indretning, der sikrer dig en behagelig og afslappende oplevelse. Vores forskellige
					værelsestyper inkluderer alt fra standardværelser til suiter og luksuslejligheder, som
					imødekommer alle dine specifikke behov. Alle værelser har et moderne badeværelse,
					fladskærms-tv, trådløst internet og andet nødvendigt udstyr. Nyd en fantastisk udsigt over
					Ilulissat by og omgivelserne fra dit værelse, og lad vores venlige personale tage sig af
					alt det praktiske. Book dit ophold på Hotel Ilulissat og få den bedste mulige oplevelse i
					hjertet af det arktiske paradis.
				</p>
			</div>
			<div class="actioncontainer">
				<button> <a href="/rooms">Book en Værelse</a> </button>
			</div>
		</div>
		<div class="card">
			<div class="titlecontainer">
				<h2>Konference</h2>
			</div>
			<img
				src="https://static.wixstatic.com/media/ca17e2_436acb3941bc46fdad0f4a6e662432fb~mv2.jpg/v1/fill/w_568,h_368,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_436acb3941bc46fdad0f4a6e662432fb~mv2.jpg"
			/>
			<div class="descriptioncontainer">
				<p>
					Hold din næste konference eller forretningsmøde på Hotel Ilulissat og få adgang til vores
					moderne konferencefaciliteter. Vi har et bredt udvalg af mødelokaler i forskellige
					størrelser, som kan imødekomme dine specifikke behov. Vores faciliteter er udstyret med
					den nyeste teknologi og moderne audio-visuelle udstyr, der sikrer en problemfri og
					professionel præsentation. Vores engagerede personale vil sørge for, at din konference
					eller dit møde forløber glat, så du kan fokusere på det, der er vigtigt for dig og din
					virksomhed. Book dine næste konferencefaciliteter på Hotel Ilulissat og oplev den perfekte
					balance mellem arbejde og afslapning i smukke omgivelser i hjertet af Ilulissat.
				</p>
			</div>
			<div class="actioncontainer">
				<button> Book her </button>
			</div>
		</div>
		<div class="card">
			<div class="titlecontainer">
				<h2>Rooftop</h2>
			</div>
			<div class="descriptioncontainer">
				<p>
					Tag med på en kulinarisk rejse på vores tagterrasse-restaurant på Hotel Ilulissat. Nyd
					vores lækre menu, som tilbyder autentiske grønlandske retter og en fantastisk udsigt over
					Ilulissat Isfjord. Vores erfarne kokke vil tage dig med på en gastronomisk oplevelse, hvor
					friske lokale råvarer og grønlandske traditioner er i fokus. Forkæl dig selv med vores
					unikke cocktails og et udvalg af vin fra hele verden. Besøg vores tagterrasse-restaurant
					og oplev en uforglemmelig aften under midnatssolen eller det magiske nordlys.
				</p>
			</div>
			<div class="actioncontainer">
				<div class="numbercontainer">
					<h3>Book et bord her: <a href="tel:+299 00 00 00">+299 00 00 00</a></h3>
				</div>
			</div>
		</div>
		<div class="card">
			<div class="titlecontainer">
				<h2>Faciliteter</h2>
			</div>
			<div class="descriptioncontainer">
				<p>
					Tag med på en kulinarisk rejse på vores tagterrasse-restaurant på Hotel Ilulissat. Nyd
					vores lækre menu, som tilbyder autentiske grønlandske retter og en fantastisk udsigt over
					Ilulissat Isfjord. Vores erfarne kokke vil tage dig med på en gastronomisk oplevelse, hvor
					friske lokale råvarer og grønlandske traditioner er i fokus. Forkæl dig selv med vores
					unikke cocktails og et udvalg af vin fra hele verden. Besøg vores tagterrasse-restaurant
					og oplev en uforglemmelig aften under midnatssolen eller det magiske nordlys.
				</p>
			</div>
			<div class="actioncontainer">
				<button> Book her </button>
			</div>
		</div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
	.numbercontainer {
		padding: 1em;
		border-radius: 20px;
		max-height: 100%;
	}

	.maincontainer {
		height: 100%;
		width: 100%;

		background-image: url('https://bgfons.com/d/ice_texture2973.jpg');
		background-size: cover;
		overflow-y: visible;
		display: flex;
	}

	.pagetitle {
		grid-column-start: 2;
		grid-column-end: 3;
		text-align: center;
		grid-column-start: 2;
		grid-column-end: 4;
		display: flex;
		justify-content: center;
		align-items: center;
		font-family: 'Oswald', sans-serif;
		font-size: xx-large;
		color: white;
	}

	a {
		color: white;
		text-decoration: none;
	}

	.grid {
		margin-inline: auto;
		max-width: 90%;
		display: grid;
		grid-template-columns: 1fr 1fr 1fr 1fr;
		grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr;
		grid-gap: 2em;

		/*make the navbar sticky*/

		top: 0;
		z-index: 1;
		width: 100%;
	}

	.card {
		font-family: 'Oswald', sans-serif;
		height: 100%;
		background-color: #003d7e9c;
		grid-row-start: 3;
		grid-row-end: 6;
		display: grid;
		border-radius: 1em;
		grid-template-rows: 10% 30% 40% 10%;

		align-items: center;
		padding: 2em;
		justify-content: center;
		color: rgb(255, 255, 255);
	}

	.titlecontainer {
		grid-column-start: 1;
		grid-column-end: 3;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.descriptioncontainer > p {
		margin-inline: 20px;
		text-align: center;
		grid-column-start: 1;
		grid-column-end: 3;
		font-size: 0.9em;
	}

	img {
		height: 100%;
		grid-column-start: 1;
		grid-column-end: 3;
	}

	.actioncontainer {
		display: flex;
		justify-content: center;
		align-items: center;
		grid-column-end: 2;
		grid-column-start: 1;
		height: 100%;
	}

	button {
		border-radius: 20px;
		width: 50%;
		height: 100%;
		background-color: rgb(106, 181, 231);
		border: none;
	}

	button:hover {
		background-color: rgb(62, 117, 189);
		box-shadow: 2px 2px 5px 1px rgba(0, 0, 0, 0.8);
		transition: ease-in 0.2s;
	}
	@media screen and (max-width: 800px) {
		.descriptioncontainer {
			font-size: 0.7em;
		}

		h3 {
			font-size: 1em;
		}

		.grid {
			display: flex;
			flex-direction: column;
			justify-content: space-around;
			padding: 20px;
		}

		.maincontainer {
			background-size: 100% 100%;
		}

		.maincontainer {
			height: auto;
		}
	}

	@media screen and (min-width: 800px) and (max-width: 1200px) {
		.grid {
			display: flex;
			flex-direction: column;
			justify-content: space-around;
			align-items: center;
			height: 100%;
		}

		.card {
			width: 50%;
			max-height: 15%;
			font-size: x-small;
			text-align: center;
		}

		.numbercontainer {
		}

		h3 {
			font-size: small;
		}

		h2 {
			font-size: large;
		}

		button {
			height: fit-content;
		}
	}
</style>
