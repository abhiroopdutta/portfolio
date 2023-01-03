<script>
	import { page } from '$app/stores';
	let path;
	$: path = $page.url.pathname;
</script>

<div class="nav-container">
	<h2 class="logo shoulder-800">AD&#8482;</h2>
	<nav>
		<a class="shoulder-800" class:active={path === '/'} href="/">Home</a>
		<a class="shoulder-800" class:active={path === '/projects'} href="/projects">Projects</a>
		<a class="shoulder-800" class:active={path === '/about'} href="/about">About</a>
	</nav>
</div>
<div class="layout">
	<slot />
</div>
<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@400;600;800&family=Bungee+Inline&family=Montserrat:wght@500&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<style>
	:root {
		--app-color: #d85c46;
		--font-color: rgb(248, 235, 188);
		--nav-color: rgb(248, 235, 188);
		--nav-text-color: #d85c46;
		--container-1-color: rgb(248, 235, 188);
		--container-2-color: rgb(248, 235, 188);
		--container-text-color: #d85c46;
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
		margin: 0 min(5vw, 3rem) min(2vh, 2rem) min(5vw, 3rem);
		border-top: 2px solid var(--font-color);
		padding-top: min(2vh, 2rem);
	}

	:global(body) {
		background-color: var(--app-color);
	}

	.nav-container {
		display: flex;
		position: sticky;
		top: 0;
		padding: min(2vh, 2rem) min(5vw, 3rem);
		background-color: var(--app-color);
		justify-content: space-between;
		align-items: center;
	}

	.logo {
		text-transform: uppercase;
		letter-spacing: 1px;
		line-height: 1;
		font-size: clamp(1.5rem, 7vw, 2.5rem);
	}

	nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: var(--nav-color);
		padding: min(7vw, 0.6rem) 1rem;
		border-radius: 26px;
		max-width: min(100vw, 20rem);
	}
	a {
		text-transform: uppercase;
		font-size: clamp(1rem, 1vw, 2rem);
		padding: 0 min(3vw, 1rem);
		color: var(--nav-text-color);
	}
	a:hover,
	.active {
		text-decoration: underline;
	}
</style>
