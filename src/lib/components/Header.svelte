<script lang="ts">
	let { 
    name = 'Thayne',
    fake_name
  }: { 
    name: string
    fake_name?: string
  } = $props()
</script>

<header class="bg-pink-700 text-white px-4 rounded-lg">
	<h1>Hello {name}</h1>

	<h2>Svelte 5 Basics</h2>
	<ul>
		<li><a href="/basics/intro">Rune: $state</a></li>
		<li><a href="/basics/derived">Rune: $derived</a></li>
		<li><a href="/basics/template_logic">Template Conditions and Logic</a></li>
	</ul>

	<br />
	<br />

	<h2>Examples</h2>
	<ul>
		<li><a href="/examples/01-counter">Counter</a></li>
		<li><a href="/examples/02-temperature-converter">Temperature Converter</a></li>
	</ul>
</header>

<style>
</style>
