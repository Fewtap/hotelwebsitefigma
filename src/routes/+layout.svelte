<script lang="ts">
	import { page } from '$app/stores';
	let url: string | null = null;
	page.subscribe((value) => {
		url = value.route.id;
	});
</script>

<nav>
	<div class="buttoncontainer">
		<button class:selected={url == '/' ? true : false}><a href="/">Hjem</a></button>
		<button class:selected={url == '/rooms' ? true : false}><a href="/rooms">Værelser</a></button>
	</div>
	<div class="logocontainer">
		<img src="https://1000logos.net/wp-content/uploads/2021/04/Best-Western-logo.png" alt="" />
	</div>
	<div id="sep" />
</nav>

<slot />

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
	$primary-color: #003d7e;

	#sep {
		height: 100%;
		width: 1px;
	}

	.buttoncontainer {
		display: flex;
		height: 100%;
		margin-left: 1em;
	}
	nav {
		height: 10%;
		display: flex;
		position: absolute;
		top: 0;
		left: 0;
		/*add border radius at bottom right and bottom left*/
		border-radius: 0 0 20px 20px;
		justify-content: space-between;
		align-items: center;

		z-index: 1;
		width: 100%;
	}

	a {
		margin: 1em;
		text-decoration: none;
		color: aliceblue;
		font-family: 'Oswald', sans-serif;
		font-size: 1.5em;
	}

	button {
		margin: 1em;
		background-color: transparent;
		height: 50%;
		border-radius: 20px;
		border: none;
	}

	.selected > a {
		color: $primary-color;
	}

	.logocontainer {
		display: flex;
		position: absolute;
		right: 0;
		margin-right: 5em;
		justify-content: center;
		align-items: center;
		height: 100%;
	}

	.logocontainer > img {
		height: 100%;
	}

	button > *:hover {
		color: gray;
	}

	@media screen and (max-width: 960px) {
		nav {
			height: 5%;
		}
		.logocontainer {
			margin-right: 1em;
		}
	}
</style>
