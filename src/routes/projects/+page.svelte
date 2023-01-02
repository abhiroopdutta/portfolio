<script>
	let data = [
		{
			title: 'ETyres',
			year: '2021',
			desc: 'Inventory/Invoicing App',
			link: '',
			technologies: ['React', 'Antd', 'Flask', 'Mongo', 'Docker']
		},
		{
			title: 'Raaga',
			year: '2022',
			desc: 'Music Tutoring App',
			link: '',
			technologies: ['React', 'React-Query', 'Bootstrap', 'Django', 'Docker']
		}
	];
</script>

<section>
	{#each data as { title, year, desc, technologies, link }}
		<article>
			<header>
				<p class="monster-500">{desc}</p>
				<p class="monster-500">{year}</p>
			</header>
			<main>
				<h1><a class="shoulder-600" href={link}>{title}</a></h1>
				<span class="material-symbols-outlined"> link </span>
			</main>
			<ul>
				{#each technologies as techonology}
					<li class="monster-500">{techonology}</li>
				{/each}
			</ul>
		</article>
	{/each}
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		gap: 2rem;
	}
	article {
		background-color: var(--container-1-color);
		padding: 2rem 2rem;
		border-radius: 26px;
	}

	article:nth-child(2) {
		background-color: var(--container-2-color);
	}
	header {
		margin-top: 1rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		align-items: baseline;
		margin-bottom: 1rem;
	}
	main {
		padding-block: 2rem;
		border-top: 2px solid var(--container-text-color);
		display: flex;
		align-items: baseline;
	}
	h1 {
		font-size: clamp(6rem, 8vw, 8rem);
		text-transform: uppercase;
		display: inline-block;
	}

	a {
		color: var(--container-text-color);
	}
	ul {
		display: inline-block;
	}

	p {
		text-transform: uppercase;
		color: var(--container-text-color);
		font-size: clamp(1rem, 1vw, 2rem);
	}

	ul {
		display: flex;
		flex-wrap: wrap;
		gap: 1rem;
		margin-bottom: 1rem;
	}

	li {
		padding: 2px 16px;
		border: 1px solid var(--container-text-color);
		border-radius: 20px;
		font-size: clamp(0.8rem, 1vw, 1rem);
		color: var(--container-text-color);
		text-transform: uppercase;
	}
</style>
