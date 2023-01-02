<div class="layout">
	<div class="nav-container">
		<h2 class="logo shoulder-600">AbhiroopDutta&#8482;</h2>
		<nav>
			<button><span class="material-symbols-outlined"> dark_mode </span></button>
			<a class="shoulder-800" href="/">Home</a>
			<a class="shoulder-800" href="/projects">Projects</a>
			<a class="shoulder-800" href="/">About</a>
		</nav>
	</div>
	<slot />
</div>
<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@400;600;800&family=Bungee+Inline&family=Montserrat:wght@500&display=swap"
		rel="stylesheet"
	/>
	<link
		rel="stylesheet"
		href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
	/>
	<link
		rel="stylesheet"
		href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
	/>
</svelte:head>

<style>
	:root {
		--app-color: #f8f8d5;
		--font-color: #3c3c3c;
		--container-1-color: rgb(253, 213, 196);
		--container-1-color: rgb(248, 219, 255);
	}
	:global(.shoulder-800) {
		font-family: 'Big Shoulders Display', cursive;
		font-weight: 800;
		color: var(--font-color);
	}
	:global(.shoulder-600) {
		font-family: 'Big Shoulders Display', cursive;
		font-weight: 600;
		color: var(--font-color);
	}
	:global(.shoulder-400) {
		font-family: 'Big Shoulders Display', cursive;
		font-weight: 400;
		color: var(--font-color);
	}
	:global(.monster-500) {
		font-family: 'Montserrat', sans-serif;
		font-weight: 500;
		color: var(--font-color);
	}
	:global(.bungee) {
		font-family: 'Bungee Inline', cursive;
		font-weight: 400;
		color: var(--font-color);
	}
	:global(*) {
		margin: 0;
		padding: 0;
		list-style: none;
		text-decoration: none;
	}
	.layout {
		margin: min(20vh, 2rem) min(5vw, 4rem);
	}

	:root {
		background-color: var(--app-color);
	}

	.nav-container {
		display: flex;
		position: sticky;
		top: min(20vh, 2rem);
	}

	.logo {
		display: none;
		line-height: 1;
	}

	@media (min-width: 40em) {
		.nav-container {
			justify-content: space-between;
			align-items: center;
		}
		.logo {
			display: block;
			font-size: 2rem;
			letter-spacing: 1px;
		}
	}

	nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #ffffff;
		padding: min(7vw, 0.6rem) 1rem;
		border: 2px solid var(--font-color);
		border-radius: 26px;
		max-width: min(100vw, 20rem);
	}
	button {
		border: none;
		background-color: transparent;
		cursor: pointer;
		display: flex;
		align-items: flex-end;
	}
	span {
		padding: 0 0 0 5px;
	}
	a {
		text-transform: uppercase;
		font-size: clamp(1rem, 1vw, 2rem);
		padding: 0 min(7vw, 1rem);
	}
</style>
