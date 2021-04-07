<script>
    let player = {
      name: "",
      points: 0
    };
</script>

<form class="grid-3">
  <input type="text" placeholder="Player Name" 
  bind:value={player.name}>
  <input type="text" placeholder="Player Points" 
  bind:value={player.name}>

</form>