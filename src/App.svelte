<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';
	import AddPlayer from './AddPlayer.svelte';

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

	const addPlayer = e => {
		const newPlayer = e.detail;

		players = [...players, newPlayer];
	};

	const removePlayer = e => {
		players = players.filter(player => player.name !== e.detail);
	};
</script>

<Navbar />
<div class="container">
	<AddPlayer on:addplayer={addPlayer} />
	{#if players.length === 0}
		<p>No Players</p>
	{:else}
		{#each players as player}
			<Player
					name={player.name}
					points={player.points}
					on:removeplayer={removePlayer}
			/>
		{/each}
	{/if}
</div>

<style>

</style>
