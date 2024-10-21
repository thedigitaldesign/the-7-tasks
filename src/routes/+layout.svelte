<script lang="ts">
  //-- Styles
	import '$lib/assets/css/tailwind.css'
  //-- Components
  import Header from '$lib/components/Header.svelte'

  const name = 'Thayne Ulysses Christensen'
</script>

<main class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
  <Header {name} />

  <slot>Oops! Something wen't wrong</slot>
</main>

<style>
  
</style>