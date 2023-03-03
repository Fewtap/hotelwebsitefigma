<script lang="ts">
	export let title: String;
	export let description: String;
	export let image: String;
</script>

<div class="card">
	<img src="${image}" />
	<div class="card-content">
		<h3>{title}</h3>
		<p>
			{description}
		</p>
	</div>
</div>

<style>
	.card {
		background-color: #f1f1f1;
		height: 400px;
		width: 100%;
		display: flex;
		align-items: center;
		margin-inline: auto;
		border-radius: 20px;

		/*add margin to the bottom of the card*/
		margin-bottom: 20px;
	}

	.card img {
		max-width: 400px;
		height: 400px;
		/*make the image have the same border radius as the card*/
		border-radius: 20px 0 0 20px;
	}

	.card-content {
		margin-inline: 20px;
		font-size: 1.3em;
	}
</style>
