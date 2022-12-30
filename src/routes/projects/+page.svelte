<script>
	const img1 = new URL('./images/createOrder.png', import.meta.url).href;
	const img2 = new URL('./images/purchase.png', import.meta.url).href;
	const img3 = new URL('./images/reports.png', import.meta.url).href;
	const img4 = new URL('./images/accounts.png', import.meta.url).href;
	let list;
	const images = [img1, img2, img3, img4];
	const handleHorizontalScroll = (evt) => {
		evt.preventDefault();
		list.scrollLeft += evt.deltaY;
	};
</script>

<section>
	<h1 class="shoulder-800">Etyres</h1>
	<p>
		Lorem ipsum dolor sit amet, consectetur adipisicing elit. Temporibus debitis totam commodi amet,
		nostrum nobis expedita veniam repudiandae ullam unde ex odio sapiente? Asperiores consequuntur
		praesentium voluptatum magni odio at! Lorem ipsum dolor sit amet, consectetur adipisicing elit.
		Temporibus debitis totam commodi amet, nostrum nobis expedita veniam repudiandae ullam unde ex
		odio sapiente? Asperiores consequuntur praesentium voluptatum magni odio at! Lorem ipsum dolor
		sit amet, consectetur adipisicing elit. Temporibus debitis totam commodi amet, nostrum nobis
		expedita veniam repudiandae ullam unde ex odio sapiente? Asperiores consequuntur praesentium
		voluptatum magni odio at! Lorem ipsum dolor sit amet, consectetur adipisicing elit. Temporibus
		debitis totam commodi amet, nostrum nobis expedita veniam repudiandae ullam unde ex odio
		sapiente? Asperiores consequuntur praesentium voluptatum magni odio at!
	</p>
	<br />
	<ul bind:this={list} on:wheel={handleHorizontalScroll}>
		{#each images as imgUrl}
			<li>
				<img src={imgUrl} alt="website" />
			</li>
		{/each}
	</ul>
</section>

<style>
	h1 {
		font-size: clamp(1rem, 12vw, 4rem);
		margin: 0 0 1rem 0;
		line-height: 0.9;
		text-transform: uppercase;
	}
	ul {
		display: flex;
		align-items: center;
		border-top: 2px solid black;
		border-bottom: 2px solid black;
		margin: 0 -2rem;
		list-style: none;
		background-color: #ffe7be;
		overflow-x: scroll;
	}

	/* Hide scrollbar for Chrome, Safari and Opera */
	ul::-webkit-scrollbar {
		display: none;
	}

	/* Hide scrollbar for IE, Edge and Firefox */
	ul {
		-ms-overflow-style: none; /* IE and Edge */
		scrollbar-width: none; /* Firefox */
	}
	img {
		margin: 2rem;
		max-width: 1000px;
		border: 2px solid black;
		border-radius: 2rem;
	}
</style>
