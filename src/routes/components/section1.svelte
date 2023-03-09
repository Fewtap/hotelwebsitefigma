<script lang="ts">
	//import inview
	import { inview } from 'svelte-inview';
	import { fade, slide } from 'svelte/transition';
	import type { ObserverEventDetails, ScrollDirection, Options } from 'svelte-inview';
	import arrow from '../../assets/images/downarrow.png';
	import blacklogo from '../../assets/images/logoblack.png';

	let isInView: boolean = false;
	let currenttime = new Date();

	function scrolltosection() {
		let section2 = document.getElementById('cardscontainer');

		section2?.scrollIntoView({ behavior: 'smooth' });
	}

	setTimeout(() => {
		isInView = true;
	}, 50);
</script>

<div class="maincontainer">
	<!--this animation should start when the page is loaded-->

	<div class="centerdiv" class:show={isInView}>
		<h1>Oplev det ultimative arktiske eventyr på</h1>
		<div id="divider" />
		<div class="logocontainer">
			<img id="logo" src={blacklogo} alt="Logo of Hotel Ilulissat" />
			<div class="buttonbookcontainer">
				<button
					><a
						href="https://www.bestwestern.dk/booking-path/hotel-rooms/best-western-plus-hotel-ilulissat-ilulissat-96100"
						>Book En værelse</a
					></button
				>
			</div>
		</div>

		<div id="button" on:click={scrolltosection}>
			<img src={arrow} />
		</div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
	h1 {
		font-family: 'Oswald', sans-serif;
		font-size: 4em;
		text-align: center;
		color: #003c7e;
	}
	.centerdiv {
		grid-template-columns: 1fr;
		grid-template-rows: 40% 1% 35% 1fr 10%;
		min-height: 80%;
		width: 60%;
		display: none;

		margin-inline: auto;
		border-radius: 10px;
	}

	.maincontainer {
		height: 100%;
		width: 100%;

		background: url('https://images.wallpaperscraft.com/image/single/whale_tail_ocean_123547_2560x1440.jpg');
		background-size: cover;
		/*make the background darker*/
	}

	h1 {
		top: auto;
		font-size: 5em;
		text-align: center;
		align-self: flex-end;
	}

	button {
		background-color: #003c7e;
		color: white;
		border: none;
		border-radius: 10px;
		padding: 10px;
		font-size: 1.5em;
		font-family: 'Oswald', sans-serif;
		transform: scale(1);
		transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.3s;
	}

	a {
		text-decoration: none;
		color: white;
	}

	.buttonbookcontainer {
		margin-top: 10%;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100%;
		width: 50%;
	}

	#button {
		margin-inline: auto;
		height: 100px;
		border-radius: 180%;
		display: flex;
		flex-direction: column;
		justify-content: end;
		align-items: end;
		margin-top: 6em;
	}

	.logocontainer {
		display: flex;
		flex-direction: column;

		justify-content: space-between;
		align-items: center;
		height: fit-content;
	}

	#divider {
		border: solid #003c7e 1px;
		width: 100%;
		height: 1px;
		background-color: #003c7e;
	}

	#button > img {
		height: 100%;
		transform: scale(1);
		transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.5s;
	}

	#button > img:hover {
		transform: scale(1.3);
		transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.5s;
	}

	img {
		margin-inline: auto;

		width: auto;
	}

	#logo {
		height: 50%;
		grid-row-start: 2;
		grid-row-end: 3;
		height: fit-content;
		margin-top: 5%;
	}

	.show {
		animation: fadein 2s;
		display: grid;
	}

	@keyframes fadein {
		from {
			opacity: 0;
			transform: scale(0);
		}
		to {
			opacity: 1;
			transform: scale(1);
		}
	}

	@media screen and (max-width: 960px) {
		h1 {
			font-size: 2em;
		}
		#logo {
			height: 5em;
		}
		.centerdiv {
			width: 90%;
		}
	}

	@media screen and (max-width: 1280px) {
		h1 {
			font-size: 2.5em;
		}
		#logo {
			height: 5em;
		}
		.centerdiv {
			width: 90%;
		}
	}

	@media screen and (min-width: 1000px) and (min-height: 800px) {
		h1 {
			font-size: 5em;
		}
		#logo {
			height: 5em;
		}
		.centerdiv {
			width: 90%;
		}
	}

	@media screen and (min-width: 2000px) {
		h1 {
			font-size: 2.5em;
		}
		#logo {
			height: 10em;
		}
		.centerdiv {
			width: 90%;
		}

		#button {
			margin-top: 15em;
		}
	}

	@media screen and (max-width: 450px) {
		h1 {
			font-size: 1.5em;
		}
	}

	button:hover {
		transform: scale(1.1);
		transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.5s;
		/*make the mouse pointer a hand*/
		cursor: pointer;
	}
</style>
