<script lang="ts">
	import Tile from '../lib/Tile.svelte';
	import TileGrid from '../lib/TileGrid.svelte';
	import LivingRoom from '../lib/LivingRoom.svelte';
</script>

<LivingRoom />
<main class="main">
	<TileGrid>
		<Tile width="1" height="1" />
		<Tile width="2" height="1" />
		<Tile width="2" height="1" />
		<Tile width="2" height="1" />
		<Tile width="1" height="2" />
	</TileGrid>
</main>

<style>
	.main {
		padding: 1rem;
		display: flex;
		justify-content: center;
	}
</style>
