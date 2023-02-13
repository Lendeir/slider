<script>
	import Section from './Section.svelte';

	let screenWidth = globalThis.window?.innerWidth;
	let screenHeight = globalThis.window?.innerHeight;

	globalThis.window?.addEventListener('resize', () => {
		screenWidth = window?.innerWidth;
		screenHeight = window?.innerHeight;
	});
</script>

{#if screenWidth > 750}
	<Section />
{/if}

{#if screenWidth < 750}
	<Section single />
{/if}
