<script>
	let data = [
		{
			title: 'ETyres',
			year: '2021',
			desc: 'Inventory/Invoicing App',
			link: 'https://github.com/abhiroopdutta/etyres',
			technologies: ['React', 'Antd', 'Flask', 'Mongo', 'Docker']
		},
		{
			title: 'Raaga',
			year: '2022',
			desc: 'Music Tutoring App',
			link: 'http://raagamedia.com/',
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
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="26"
					height="26"
					fill="currentColor"
					class="bi bi-box-arrow-up-right"
					viewBox="0 0 16 16"
				>
					<path
						fill-rule="evenodd"
						d="M8.636 3.5a.5.5 0 0 0-.5-.5H1.5A1.5 1.5 0 0 0 0 4.5v10A1.5 1.5 0 0 0 1.5 16h10a1.5 1.5 0 0 0 1.5-1.5V7.864a.5.5 0 0 0-1 0V14.5a.5.5 0 0 1-.5.5h-10a.5.5 0 0 1-.5-.5v-10a.5.5 0 0 1 .5-.5h6.636a.5.5 0 0 0 .5-.5z"
					/>
					<path
						fill-rule="evenodd"
						d="M16 .5a.5.5 0 0 0-.5-.5h-5a.5.5 0 0 0 0 1h3.793L6.146 9.146a.5.5 0 1 0 .708.708L15 1.707V5.5a.5.5 0 0 0 1 0v-5z"
					/>
				</svg>
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
		padding: min(8vw, 2rem);
		border-radius: 26px;
		box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
		transition: 0.5s;
	}

	article:nth-child(2) {
		background-color: var(--container-2-color);
	}
	article:hover {
		transform: translate(0, -4px);
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
		gap: 5px;
		flex-wrap: wrap;
		align-items: baseline;
	}
	h1 {
		font-size: clamp(6rem, 8vw, 8rem);
		text-transform: uppercase;
		display: inline-block;
	}
	.bi {
		color: var(--container-text-color);
		fill: var(--container-text-color);
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
