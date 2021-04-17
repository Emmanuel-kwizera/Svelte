<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';
  import AddPlayer from './AddPlayer.svelte';

  let showForm = false;
	let players = [
    {
      name: "John Doe",
      points: 53
    },
    {
      name: "Sam Smith",
      points: 45
    },
    {
      name: "Sara Wilson",
      points: 34
    }
  ];
  
  const addPlayer = e => {
    const newPlayer = e.detail;
    players = [...players,newPlayer];
  }
  const removePlayer = e => {
    players = players.filter(player => player.name !== e.detail);
  };
  const triggerShowForm = () => (showForm = !showForm);
</script>
<main>
	<Navbar />
  <div class="container">
    <button class="btn btn-info" on:click={triggerShowForm}>Add player</button>
    {#if showForm}
      <AddPlayer on:addplayer={addPlayer}/>    
    {/if}
  </div>
	<div class="container">
		{#if players.length === 0}
			<p>No Players</p>
			{:else}
				{#each players as player}
					<Player name = {player.name} points={player.points} on:removeplayer={removePlayer}/>
				{/each}
		{/if}
	</div>
</main>

<style>

</style>