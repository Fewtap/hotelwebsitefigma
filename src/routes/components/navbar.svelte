<script lang="ts">
</script>

<div class="navbar">
	<div class="container links">
		<button><a href="/">Home</a></button>
		<button><a href="/about">About</a></button>
		<button><a href="/contact">Contact</a></button>
		<button><a href="/login">Login</a></button>
	</div>
	<div class="container">
		<img
			src="https://static.wixstatic.com/media/015531_11331bde76244c9db30c799c6b22fc00~mv2.png/v1/fill/w_363,h_127,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Hotel%20Ilulissat%20Logo%20-SORTSKRIFT.png"
		/>
	</div>
	<div class="container" />
</div>

<style>
	.navbar {
		height: 3em;
		border: 1px solid black;
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: 1fr;
		grid-gap: 10px;
		object-fit: contain;
		background-color: #2365a75c;
		/*make the navbar sticky*/
		position: sticky;
		top: 0;
		z-index: 1;
	}

	.container {
		height: 100%;
		border: 1px solid black;
		/*the container cannot be higher than the navbar*/
		overflow: hidden;
	}

	.links {
		display: flex;
		justify-content: space-evenly;
		align-items: center;
	}

	.links button {
		background-color: rgb(73, 159, 187);
		border-radius: 10px;
		width: 6em;
		height: 2em;
		color: white;
		border: none;
	}

	.links button:hover {
		background-color: #4869dd;
		color: white;
		transform: scale(1.1);
		transition: 0.2s;
	}

	img {
		display: block;
		height: 100%;
		width: auto;
		object-fit: contain;
		margin-inline: auto;
	}

	/*the buttons need to scale up when hovered over*/

	.links a {
		text-decoration: none;
		color: white;
	}
</style>
