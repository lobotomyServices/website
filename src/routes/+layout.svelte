<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import '@fontsource/poppins';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav class="p-4 flex flex-col gap-4 items-center md:grid md:grid-cols-2 md:justify-items-center bg-slate-900">
  <section id="home" class="md:justify-self-start">
    <a href="/">Lobotomy Services</a>
  </section>
  <section id="links" class="flex flex-col md:flex-row md:justify-self-end gap-4">
    <a href="/">Lobotomy Services</a>
    <a href="/">Lobotomy Services</a>
    <a href="/">Lobotomy Services</a>
  </section>
</nav>

<div id="wrapper" class="grid grid-rows-[1fr 1fr] gap-8 justify-self-center justify-items-center max-w-4xl p-8">
  {@render children()}

  <footer class="grid grid-rows-2 gap-2 justify-items-center text-sm">
    <p class="min-h-0">Licensed under the EUPL</p>
    <a class="min-h-0 self-start" href="https://github.com/lobotomyServices/lobotomyservices.github.io">See the source code.</a>
  </footer>
</div>
