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
	<Player />
</div>

<style>

</style>
