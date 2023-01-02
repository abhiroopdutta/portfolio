<section class="home-page">
	<header>
		<h1 class="profession-first bungee">Web</h1>
		<h1 class="profession-last bungee">Developer</h1>
	</header>

	<article>
		<section class="name-skills">
			<h1 class="name shoulder-600">Abhiroop</h1>
			<ul>
				<li class="shoulder-600">react</li>
				<li class="shoulder-600">flask</li>
				<li class="shoulder-600">mongo</li>
				<li class="shoulder-600">mysql</li>
				<li class="shoulder-600">docker</li>
				<li class="shoulder-600">nginx</li>
				<li class="shoulder-600">git</li>
				<li class="shoulder-600">bash</li>
				<li class="shoulder-600">aws ec2</li>
			</ul>
		</section>
		<address class="shoulder-600">India, 2023</address>
	</article>
</section>

<style>
	.home-page {
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
		line-height: 0.75;
	}
	.profession-last {
		font-size: clamp(2.4rem, 6vw, 10rem);
		padding-top: 1rem;
		line-height: 1;
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
			font-size: 6vh;
			font-style: normal;
			text-transform: uppercase;
			line-height: 0.9;
		}
	}
</style>
