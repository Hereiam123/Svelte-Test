<script>
  export let name;
  export let points;
  let showControls = false;

  const addPoint = () => points++;
  const removePoint = () => points--;
  const toggleControls = () => (showControls = !showControls);
</script>

<style>
  h1 {
    color: blue;
  }
</style>

<div class="card">
  <h1>
     {name}
    <button class="btn-sm" on:click={toggleControls}>
      {#if showControls}-{:else}+{/if}
    </button>
  </h1>
  <h3>Points: {points}</h3>
  {#if showControls}
    <button class="btn" on:click={addPoint}>+1</button>
    <button class="btn btn-dark" on:click={removePoint}>-1</button>
    <input type="number" bind:value={points} />
  {/if}
</div>
