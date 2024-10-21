<script lang="ts">
  let celsius = $state(0)
  let fahrenheit = $state(0)
</script>

<div>
  <input type="number" bind:value={celsius} /> Celsius =
  <input type="number" bind:value={fahrenheit} /> Fahrenheit
</div>

<style>
  
</style>