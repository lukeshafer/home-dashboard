<script lang="ts">
	export let height: '1' | '2';
	export let width: '1' | '2';

	width = +width > 1 ? '2' : '1';
	height = +height > 1 ? '2' : '1';
</script>

<div class="tile" style:--w={width} style:--h={height}>
	<slot><span class="fallback">Whoops! You forgot to add a child to this tile!</span></slot>
</div>

<style>
	.tile {
		background-color: blue;
		border-radius: 2rem;
		width: calc(var(--w) * var(--tile-base-size, 8rem) + (var(--w) - 1) * var(--tile-gap, 3rem));
		height: calc(var(--h) * var(--tile-base-size, 8rem) + (var(--h) - 1) * var(--tile-gap, 3rem));

		grid-column: span var(--w);
		grid-row: span var(--h);
	}

	.fallback {
		display: flex;
		font-size: 1.5rem;
		align-items: center;
		justify-content: center;
		color: white;
		text-align: center;
		max-width: 70%;
		height: 100%;
		margin: 0 auto;
	}
</style>
