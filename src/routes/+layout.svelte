<div class="layout">
	<div class="nav-container">
		<nav>
			<a href="/">Home</a>
			<a href="/">Projects</a>
			<a href="/">About</a>
		</nav>
	</div>
	<slot />
</div>
<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@600;800&family=Bungee+Shade&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<style>
	.layout {
		margin: min(20vh, 2rem) min(5vw, 2rem);
	}
	:global(.shoulder-800) {
		font-family: 'Big Shoulders Display', cursive;
		font-weight: 600;
		line-height: 1;
	}
	:global(*) {
		margin: 0;
		padding: 0;
	}

	.nav-container {
		display: flex;
		position: sticky;
		top: min(20vh, 2rem);
	}

	@media (min-width: 40em) {
		.nav-container {
			justify-content: end;
		}
	}

	nav {
		display: flex;
		justify-content: space-between;
		background-color: #ffe7be;
		padding: 0.8rem 1rem;
		border: 2px solid #3d3c3c;
		border-radius: 26px;
		max-width: min(100vw, 20rem);
	}

	a {
		text-decoration: none;
		text-transform: uppercase;
		font-family: 'Big Shoulders Display', cursive;
		font-size: clamp(1rem, 1vw, 2rem);
		font-weight: 800;
		color: #3d3c3c;
		padding: 0 min(6vw, 1.5rem);
	}
</style>
