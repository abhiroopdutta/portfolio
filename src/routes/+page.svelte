<section class="parent-section">
	<section class="left-panel">
		<header>
			<h1 class="profession-first bungee">Web</h1>
			<h1 class="profession-last bungee">Developer</h1>
		</header>

		<article>
			<section class="name-skills">
				<h1 class="name shoulder-600">Abhiroop</h1>
				<ul>
					<li>react</li>
					<li>flask</li>
					<li>mongo</li>
					<li>mysql</li>
					<li>docker</li>
					<li>nginx</li>
					<li>git</li>
					<li>bash</li>
					<li>aws ec2</li>
				</ul>
			</section>
			<address>India, 2023</address>
		</article>
	</section>

	<section class="right-panel" />
</section>

<style>
	:root {
		background-color: #fff5ba;
	}

	.bungee {
		font-family: 'Bungee Shade', cursive;
		font-weight: 400;
	}

	.right-panel {
		display: none;
	}

	@media (min-width: 50em) {
		.right-panel {
			display: flex;
			justify-content: flex-end;
		}
	}

	.left-panel {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		gap: 1rem;
	}

	header {
		display: flex;
		flex-direction: column;
	}

	.profession-first {
		font-size: clamp(5rem, 6vw, 10rem);
		line-height: 1.2;
	}
	.profession-last {
		font-size: clamp(2.4rem, 6vw, 10rem);
		line-height: 1.2;
	}

	article {
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
	}

	.name-skills {
		display: flex;
		align-items: flex-end;
		gap: 1rem;
	}

	.name {
		writing-mode: vertical-lr;
		transform: rotate(180deg);
		text-transform: uppercase;
		font-size: 20vh;
		line-height: 0.9;
	}

	li {
		font-family: 'Big Shoulders Display', cursive;
		font-weight: 600;
		font-size: 4vh;
		letter-spacing: 1rem;
		text-transform: uppercase;
	}
	address {
		display: none;
	}
	@media (min-width: 50em) {
		address {
			display: block;
			font-family: 'Big Shoulders Display', cursive;
			font-weight: 600;
			font-size: 6vh;
			font-style: normal;
			text-transform: uppercase;
			line-height: 0.9;
		}
	}
</style>
