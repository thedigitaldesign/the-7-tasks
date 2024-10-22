<script lang="ts">
	//-- Styles
	import '$lib/assets/css/tailwind.css'
	//-- Components
	import Header from '$lib/components/Header.svelte'

	const name = '-- Passing a prop name --'
</script>

<main class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
	<Header {name}>
		<p>Hello!</p>
		{#snippet second_child(phrase: string)}
			<h1>{phrase}</h1>
		{/snippet}
	</Header>

	<div class="my-4">
		<slot>Oops! Something wen't wrong</slot>
	</div>
</main>

<style>
</style>
