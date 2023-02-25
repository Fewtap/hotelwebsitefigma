<script lang="ts">
	//import inview
	import { inview } from 'svelte-inview';
	import { fade, slide } from 'svelte/transition';
	import type { ObserverEventDetails, ScrollDirection, Options } from 'svelte-inview';

	let isInView: boolean = true;
	let scrollDirection: ScrollDirection;
	const options: Options = {
		rootMargin: '50px',
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
		<img
			src="https://static.wixstatic.com/media/015531_11331bde76244c9db30c799c6b22fc00~mv2.png/v1/fill/w_363,h_127,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Hotel%20Ilulissat%20Logo%20-SORTSKRIFT.png"
			alt="Logo of Hotel Ilulissat"
		/>
	</div>
</div>

<style>
	.maincontainer {
		height: 100%;
		border: 1px solid black;
		background: url('https://wallpapercave.com/wp/wp2378345.jpg');
		background-size: cover;
		overflow-y: visible;
		display: flex;
	}

	.centerdiv {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 80%;
		width: 60%;

		margin: auto;
		border-radius: 10px;
	}

	.show {
		animation: fadein 2s;
	}

	h1:hover {
		transform: scale(1.3);
		animation: scaleUp 2s;
	}

	@keyframes fadein {
		from {
			opacity: 0;
			transform: scale(0);
			transform: rotate(180deg);
		}
		to {
			opacity: 1;
			transform: scale(1);
			transform: rotate(0deg);
		}
	}
</style>
