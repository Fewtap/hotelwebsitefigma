<div class="container" id="cardscontainer">
	<div class="titlecontainer">
		<h1>Faciliteter</h1>
	</div>
	<div class="card">
		<img
			src="https://static.wixstatic.com/media/ca17e2_8e4acaa6ec2a485eab8ca4b038645c56~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_8e4acaa6ec2a485eab8ca4b038645c56~mv2.jpg"
			alt="Image 1"
		/>
		<h2>Værelser</h2>
		<div class="descriptioncontainer">
			<p>
				Oplev ultimativ komfort og afslapning på Hotel Ilulissats værelser. Vores værelser er
				designet til at give dig den perfekte kombination af moderne faciliteter og hyggelig
				indretning, der sikrer dig en behagelig og afslappende oplevelse. Vores forskellige
				værelsestyper inkluderer alt fra standardværelser til suiter og luksuslejligheder, som
				imødekommer alle dine specifikke behov. Alle værelser har et moderne badeværelse,
				fladskærms-tv, trådløst internet og andet nødvendigt udstyr. Nyd en fantastisk udsigt over
				Ilulissat by og omgivelserne fra dit værelse, og lad vores venlige personale tage sig af alt
				det praktiske. Book dit ophold på Hotel Ilulissat og få den bedste mulige oplevelse i
				hjertet af det arktiske paradis.
			</p>
		</div>
		<a href="/rooms" class="button">Vis mer information</a>
	</div>
	<div class="card">
		<img
			src="https://static.wixstatic.com/media/ca17e2_436acb3941bc46fdad0f4a6e662432fb~mv2.jpg/v1/fill/w_568,h_368,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_436acb3941bc46fdad0f4a6e662432fb~mv2.jpg"
			alt="Image 2"
		/>
		<h2>Konference</h2>
		<div class="descriptioncontainer">
			<p>
				Hold din næste konference eller forretningsmøde på Hotel Ilulissat og få adgang til vores
				moderne konferencefaciliteter. Vi har et bredt udvalg af mødelokaler i forskellige
				størrelser, som kan imødekomme dine specifikke behov. Vores faciliteter er udstyret med den
				nyeste teknologi og moderne audio-visuelle udstyr, der sikrer en problemfri og professionel
				præsentation. Vores engagerede personale vil sørge for, at din konference eller dit møde
				forløber glat, så du kan fokusere på det, der er vigtigt for dig og din virksomhed. Book
				dine næste konferencefaciliteter på Hotel Ilulissat og oplev den perfekte balance mellem
				arbejde og afslapning i smukke omgivelser i hjertet af Ilulissat.
			</p>
		</div>
		<a href="#" class="button">Vis mer information</a>
	</div>
	<div class="card">
		<img
			src="https://static.wixstatic.com/media/015531_4fa07ecc0c9f4de8921c59effa776ab8~mv2.jpg/v1/crop/x_0,y_304,w_6016,h_3409/fill/w_443,h_250,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/DSC_9305.jpg"
			alt="Image 3"
		/>
		<h2>Rooftop</h2>
		<div class="descriptioncontainer">
			<p>
				Tag med på en kulinarisk rejse på vores tagterrasse-restaurant på Hotel Ilulissat. Nyd vores
				lækre menu, som tilbyder autentiske grønlandske retter og en fantastisk udsigt over
				Ilulissat Isfjord. Vores erfarne kokke vil tage dig med på en gastronomisk oplevelse, hvor
				friske lokale råvarer og grønlandske traditioner er i fokus. Forkæl dig selv med vores
				unikke cocktails og et udvalg af vin fra hele verden. Besøg vores tagterrasse-restaurant og
				oplev en uforglemmelig aften under midnatssolen eller det magiske nordlys.
			</p>
		</div>
		<a href="#" class="button">Book et bord på +299 00 00 00</a>
	</div>
	<div class="card">
		<img
			src="https://static.wixstatic.com/media/015531_2f75ef01eaff482ea6d8ab3eb013aec4~mv2.jpg/v1/fill/w_443,h_250,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/DSC_8863.jpg"
			alt="Image 4"
		/>
		<h2>Faciliteter</h2>
		<div class="descriptioncontainer">
			<p>
				Tag med på en kulinarisk rejse på vores tagterrasse-restaurant på Hotel Ilulissat. Nyd vores
				lækre menu, som tilbyder autentiske grønlandske retter og en fantastisk udsigt over
				Ilulissat Isfjord. Vores erfarne kokke vil tage dig med på en gastronomisk oplevelse, hvor
				friske lokale råvarer og grønlandske traditioner er i fokus. Forkæl dig selv med vores
				unikke cocktails og et udvalg af vin fra hele verden. Besøg vores tagterrasse-restaurant og
				oplev en uforglemmelig aften under midnatssolen eller det magiske nordlys.
			</p>
		</div>
		<a href="#" class="button">Vis mer information</a>
	</div>
</div>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
	//create a variable that holds the primary color
	$primary-color: #003d7e;
	$secondary-color: #f2f2f2;

	.container {
		height: 100%;
		display: grid;
		grid-template-rows: 1fr 1fr 1fr;
		grid-template-columns: 1fr 1fr 1fr 1fr;
		justify-content: center;
		align-items: center;
		background: url('https://bgfons.com/d/ice_texture2973.jpg');
		background-size: cover;
	}

	.titlecontainer {
		grid-row-start: 1;
		grid-row-end: 2;
		grid-column-start: 1;
		grid-column-end: 5;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100%;
		background-color: #003d7e79;
		width: fit-content;
		height: fit-content;
		margin-inline: auto;
		border-radius: 20px;
		padding-inline: 2%;
	}

	h1 {
		font-family: 'Oswald', sans-serif;
		font-weight: SemiBold 600;
		font-size: 3em;
		color: white;
	}
	.card {
		border-radius: 5px;

		margin: 10px;
		width: 80%;
		margin-inline: auto;
		display: grid;
		grid-template-rows: 30% 7% 40% 23%;
		height: 100%;
		grid-row-start: 2;
		grid-row-end: 4;
		border-radius: 20px;
		background-color: #003d7e9c;
		font-family: 'Oswald', sans-serif;
		color: white;
		margin-bottom: 10%;
	}

	.descriptioncontainer {
		height: 100%;
		padding: 2%;
	}
	.card img {
		width: 100%;
		height: 100%;

		/*make the image border radius match the card border radius*/
		border-radius: 20px 20px 0 0;
	}
	.card h2 {
		font-size: 1.8em;
		text-align: left;
		margin: 20px;
	}
	.card p {
		margin: 5%;
		font-size: 1em;
		font-weight: 300;
	}
	.card a.button {
		font-family: 'Oswald', sans-serif;
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: #4caf50;
		color: white;
		padding: auto;
		text-align: center;
		text-decoration: none;
		border-radius: 5px;
		width: 60%;
		margin-inline: auto;
		height: 20%;
		/*center the button*/
		margin: auto;
	}

	a {
		text-decoration: none;
		color: white;
		font-family: 'Oswald', sans-serif;
	}

	@media screen and (max-width: 900px) {
		#cardscontainer {
			display: flex;
			flex-direction: column;
			justify-content: start;
			background-size: cover;
			background-repeat: repeat-y;
			height: fit-content;
			padding-top: 20px;
			padding-bottom: 20px;
		}

		.card {
			width: 80%;
			height: 30%;
			font-size: 0.3rem;
			margin: 10px;
			padding: 10px;
			/*only have 3 rows in the card*/
			grid-template-rows: 10% 70% 20%;
			background-color: #003d7e;
		}

		img {
			/*disable the image */
			display: none;
		}

		.card h2 {
			font-size: 2.5em;
			text-align: center;
			margin: 20px;
		}

		h1 {
			font-size: 1.7em;
		}

		.descriptioncontainer {
			height: 100%;
			padding: 5%;
		}

		.card p {
			margin: 10%;
			font-size: 2.5em;
			font-weight: 300;
		}

		.button {
			display: flex;
			justify-content: center;
			align-items: center;
			font-size: 1.5em;
			min-height: 50%;
			max-width: 20%;
		}
	}

	@media screen and (max-height: 1500px) and (min-width: 1000px) {
		.card p {
			font-size: 0.8em;
		}

		.card {
			width: 95%;
		}
	}
</style>
