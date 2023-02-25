<div class="maincontainer">
	<div class="grid">
		<div class="card">Card</div>
		<div class="card">Card</div>
		<div class="card">Card</div>
	</div>
</div>

<style>
	.maincontainer {
		height: 100%;
		width: 100%;
		border: 1px solid black;
		background: url('https://wallpapercave.com/wp/wp2378345.jpg');
		background-size: cover;
		overflow-y: visible;
		display: flex;
	}

	.grid {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: 1fr 1fr 1fr;
		grid-gap: 10px;
		object-fit: contain;
		background-color: #2365a75c;
		/*make the navbar sticky*/
		position: sticky;
		top: 0;
		z-index: 1;
		width: 100%;
		/*Make the card take up the two lower rows*/
	}

	.card {
		height: 100%;
		border: 1px solid black;
		grid-row-start: 2;
		grid-row-end: 3;
	}

	.card:hover {
		transform: scale(1.1);
		transition: 0.2s;
	}
</style>
