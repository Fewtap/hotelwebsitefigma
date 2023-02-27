<div id="roomscontainer">
	<div class="information">
		<h1>Værelser</h1>
		<p>alskdjalskdjalsdjalksjd</p>
	</div>
	<div class="roomscontainer">
		<div class="room">
			<div class="imgcontainer">
				<img
					src="https://static.wixstatic.com/media/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg"
				/>
			</div>
			<div class="textcontainer">
				<h2>Standard Værelse</h2>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quas possimus facilis expedita
					consectetur molestiae modi quis. Eos, obcaecati tempore totam culpa temporibus non saepe,
					illum autem voluptates cupiditate, delectus unde!
				</p>
			</div>
		</div>
		<div class="room">
			<div class="imgcontainer">
				<img
					src="https://static.wixstatic.com/media/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg"
				/>
			</div>
			<div class="textcontainer">
				<h2>Standard Værelse</h2>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quas possimus facilis expedita
					consectetur molestiae modi quis. Eos, obcaecati tempore totam culpa temporibus non saepe,
					illum autem voluptates cupiditate, delectus unde!
				</p>
			</div>
		</div>
		<div class="room">
			<div class="imgcontainer">
				<img
					src="https://static.wixstatic.com/media/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg"
				/>
			</div>
			<div class="textcontainer">
				<h2>Standard Værelse</h2>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quas possimus facilis expedita
					consectetur molestiae modi quis. Eos, obcaecati tempore totam culpa temporibus non saepe,
					illum autem voluptates cupiditate, delectus unde!
				</p>
			</div>
		</div>
		<div class="room">
			<div class="imgcontainer">
				<img
					src="https://static.wixstatic.com/media/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg/v1/fill/w_620,h_400,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ca17e2_34a2a5c8462b4ae99aad92f6c1b93412~mv2.jpg"
				/>
			</div>
			<div class="textcontainer">
				<h2>Standard Værelse</h2>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quas possimus facilis expedita
					consectetur molestiae modi quis. Eos, obcaecati tempore totam culpa temporibus non saepe,
					illum autem voluptates cupiditate, delectus unde!
				</p>
			</div>
		</div>
	</div>
</div>

<style>
	#roomscontainer {
		display: grid;
		grid-template-columns: 30% 10% 60%;
	}

	.information {
		text-align: center;
	}

	.roomscontainer {
		padding-top: 500px;
		grid-column-start: 3;
		grid-column-end: 4;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		overflow: auto;
		height: 500px;
	}

	.textcontainer {
		width: 100%;
		grid-column-start: 2;
		grid-column-end: 3;
		font-size: 3em;
	}

	.imgcontainer > img {
		max-width: 100%;
		max-height: 100%;
	}

	.imgcontainer {
		height: 100%;
		width: 100%;
		grid-column-start: 1;
		grid-column-end: 2;
	}

	.room {
		background-color: antiquewhite;
		border: solid black 1px;
		width: 100%;
		display: grid;
		grid-template-columns: 20% 1fr;
	}
</style>
