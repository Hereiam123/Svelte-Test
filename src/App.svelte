<script>
  import Navbar from "./Navbar.svelte";
  import Player from "./Player.svelte";

  let players = [{ name: "John", points: 5 }, { name: "Jane", points: 10 }];
</script>

<style>

</style>

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
