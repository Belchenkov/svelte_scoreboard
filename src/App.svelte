<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';

	let players = [
		{
			name: 'Make Smith',
			points: 34
		},
		{
			name: 'Jessica Will',
			points: 56
		},
		{
			name: 'Bob Carrol',
			points: 26
		}
	];
</script>

<Navbar />
<div class="container">
	{#if players.length === 0}
		<p>No Players</p>
	{:else}
		{#each players as player}
			<Player name={player.name} points={player.points} />
		{/each}
	{/if}
</div>

<style>

</style>
