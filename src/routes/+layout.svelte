<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import '@fontsource/poppins';
	import { resolve } from '$app/paths';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav
	class="flex flex-col items-center gap-4 bg-slate-900 p-4 md:grid md:grid-cols-2 md:justify-items-center"
>
	<section id="home" class="md:justify-self-start">
		<a href={resolve('/')}>Lobotomy Services</a>
	</section>
	<section id="links" class="flex flex-col gap-4 md:flex-row md:justify-self-end">
		<a href={resolve('/team')}>Team</a>
	</section>
</nav>

<div
	id="wrapper"
	class="grid-rows-[1fr 1fr] grid max-w-4xl justify-items-center gap-8 justify-self-center p-8"
>
	{@render children()}

	<footer class="grid grid-rows-2 justify-items-center gap-2 text-sm">
		<p class="min-h-0">Licensed under the EUPL</p>
		<a
			class="min-h-0 self-start"
			href="https://github.com/lobotomyServices/lobotomyservices.github.io">See the source code.</a
		>
	</footer>
</div>
