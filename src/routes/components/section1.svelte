<script lang="ts">
	//import inview
	import { inview } from 'svelte-inview';
	import { fade, slide } from 'svelte/transition';
	import type { ObserverEventDetails, ScrollDirection, Options } from 'svelte-inview';
	import arrow from '../../assets/images/downarrow.png';
	import blacklogo from '../../assets/images/logoblack.png';

	let isInView: boolean = false;

	function scrolltosection() {
		let section2 = document.getElementById('cardscontainer');

		section2?.scrollIntoView({ behavior: 'smooth' });
	}

	setTimeout(() => {
		isInView = true;
	}, 500);
</script>

<div class="maincontainer">
	<!--this animation should start when the page is loaded-->

	<div class="centerdiv" class:show={isInView}>
		<h1>Oplev det ultimative arktiske eventyr på</h1>
		<div id="divider" />
		<img id="logo" src={blacklogo} alt="Logo of Hotel Ilulissat" />
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
		grid-template-rows: 45% 1fr 40% 5%;
		height: 100%;
		width: 60%;
		display: none;
		margin: auto;
		border-radius: 10px;
	}

	.maincontainer {
		height: 100%;
		width: 100%;

		background: url('https://images.pexels.com/photos/53389/iceberg-antarctica-polar-blue-53389.jpeg?cs=srgb&dl=pexels-pixabay-53389.jpg&fm=jpg');
		background-size: cover;
		/*make the background darker*/

		display: flex;
	}

	h1 {
		top: auto;
		font-size: 4em;
		text-align: center;
		align-self: flex-end;
	}

	#button {
		margin-inline: auto;
		border-radius: 180%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	#divider {
		border: solid #003c7e 1px;
		width: 100%;
		height: 1px;
		background-color: #003c7e;
	}

	#button > img {
		height: 100%;
	}

	img {
		margin-inline: auto;

		width: auto;
	}

	#logo {
		height: 50%;
		top: 0;
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
			font-size: 1.5em;
		}

		.centerdiv {
			margin-inline: auto;
		}

		.centerdiv > img {
			width: auto;
			max-height: 25%;
		}

		#button > img {
			height: 100%;
		}
	}
</style>
