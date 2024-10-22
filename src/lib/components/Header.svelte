<script lang="ts">
	import type { Snippet } from "svelte"
	let { 
    name = 'Thayne',
    fake_name,
		children,
		second_child
  }: { 
    name: string
    fake_name?: string
		children: Snippet,
		second_child: Snippet
  } = $props()
</script>

<header class="bg-pink-700 text-white px-4 rounded-lg">
	<h1>{@render children()} {name}</h1>

	{@render second_child('Me hahahah')}

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
