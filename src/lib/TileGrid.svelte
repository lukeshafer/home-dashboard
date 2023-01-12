<section class="tile-grid">
	<slot />
</section>

<style>
	.tile-grid {
		--tile-base-size: 18rem;
		--tile-gap: 3rem;
		display: grid;
		grid-auto-flow: dense;
		gap: var(--tile-gap);
		grid-template-columns: repeat(auto-fill, var(--tile-base-size));

		justify-content: center;
		justify-items: center;

		max-width: 80rem;
	}
</style>
