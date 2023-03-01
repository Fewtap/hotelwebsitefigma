<script lang="ts">
	import { page } from '$app/stores';
	let url: string | null = null;
	page.subscribe((value) => {
		url = value.route.id;
	});
</script>

<nav>
	<button class:selected={url == '/' ? true : false}><a href="/">Hjem</a></button>
	<button class:selected={url == '/rooms' ? true : false}><a href="/rooms">Værelser</a></button>
</nav>

<slot />

<style>
	nav {
		height: 5%;
		display: flex;
		position: absolute;
		top: 0;
		left: 0;
		/*add border radius at bottom right and bottom left*/
		border-radius: 0 0 20px 20px;
		justify-content: center;
		align-items: center;
		background-color: #302f2f6e;
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
		background-color: #6b6a6a;
		color: aliceblue;
		height: 50%;
		border-radius: 20px;
	}

	.selected {
		border: black solid 1px;
		background-color: rgb(197, 195, 195);
	}

	button:hover {
		background-color: #b4b4b4;
	}
</style>
