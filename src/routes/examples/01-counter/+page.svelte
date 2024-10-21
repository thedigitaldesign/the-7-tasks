<script lang="ts">
  let count = $state(0)
</script>

<div>
  <input type="number" bind:value={count} disabled />
  <button onclick="{() => count++}">Increment</button>
</div>

<style>
  
</style>