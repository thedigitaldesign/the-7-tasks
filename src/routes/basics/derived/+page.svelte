<script lang="ts">
	let name = 'Thayne'

  // Derived stores are reactive stores that are derived from other stores.
	let full_name = $derived(name + ' ' + 'Ulysses Christensen')
</script>

<div>
  <h2>{full_name}</h2>
</div>

<style>
</style>
