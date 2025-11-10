<script lang="ts">
	import { page } from '$app/state';
</script>

<article class="flex flex-col items-center gap-4">
	<header class="flex flex-col items-center gap-2">
		<strong class="text-5xl text-red-500">{page.status}: {page.error.message}</strong>
		<p class="text-xs">We apologise for your failed expedition :(</p>
	</header>
</article>
