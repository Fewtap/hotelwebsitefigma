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

<style>
	#sep {
		height: 100%;
		width: 1px;
	}

	.buttoncontainer {
		display: flex;
		height: 100%;
	}
	nav {
		height: 5%;
		display: flex;
		position: absolute;
		top: 0;
		left: 0;
		/*add border radius at bottom right and bottom left*/
		border-radius: 0 0 20px 20px;
		justify-content: space-between;
		align-items: center;
		background-color: #003d7e9c;
		z-index: 1;
		width: 100%;
	}

	a {
		margin: 1em;
		text-decoration: none;
		color: aliceblue;
	}

	button {
		margin: 1em;
		background-color: #004c9e;
		color: aliceblue;
		height: 50%;
		border-radius: 20px;
		border: none;
	}

	.selected {
		background-color: #00799e;
	}

	.logocontainer {
		display: flex;
		position: absolute;
		right: 0;
		margin: 2%;
		justify-content: center;
		align-items: center;
		height: 100%;
	}

	.logocontainer > img {
		height: 100%;
	}

	button:hover {
		background-color: #1479e6;
	}
</style>
