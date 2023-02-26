<script lang="ts">
	//import inview
	import { inview } from 'svelte-inview';
	import { fade, slide } from 'svelte/transition';
	import type { ObserverEventDetails, ScrollDirection, Options } from 'svelte-inview';
	import { onMount } from 'svelte';
	import Vague from 'vague';

	let isInView: boolean = true;
	let scrollDirection: ScrollDirection;
	const options: Options = {
		rootMargin: '-50px',
		unobserveOnEnter: false
	};

	const handleChange = ({ detail }: CustomEvent<ObserverEventDetails>) => {
		isInView = detail.inView;
		scrollDirection = detail.scrollDirection.vertical;
	};
</script>

<div class="maincontainer" use:inview on:change={handleChange}>
	<!--this animation should start when the page is loaded-->

	<div class="centerdiv" transition:slide use:inview on:change={handleChange} class:show={isInView}>
		<h1>Oplev det ultimative arktiske eventyr på</h1>
		<div id="divider" />
		<img
			src="https://static.wixstatic.com/media/015531_11331bde76244c9db30c799c6b22fc00~mv2.png/v1/fill/w_363,h_127,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Hotel%20Ilulissat%20Logo%20-SORTSKRIFT.png"
			alt="Logo of Hotel Ilulissat"
		/>
	</div>
</div>

<style>
	.maincontainer {
		height: 100%;

		background: url('https://wallpapercave.com/wp/wp2378345.jpg');
		background-size: cover;
		backdrop-filter: blur(50px);

		display: flex;
	}

	h1 {
		top: auto;
		font-size: 4em;
		text-align: center;
		align-self: flex-end;
	}
	.centerdiv {
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 45% 1fr 45%;
		height: 80%;
		width: 60%;

		margin: auto;
		border-radius: 10px;
	}

	#divider {
		border: solid black 1px;
		width: 100%;
		height: 0px;
	}

	img {
		top: 0;
		margin-inline: auto;
	}

	.show {
		animation: fadein 2s;
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
</style>
