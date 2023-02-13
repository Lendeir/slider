<script>
	import Bar from './Bar.svelte';
	import Content from './Content.svelte';
	import Content2 from './Content2.svelte';

	export let single = false;
	let activeId = '0';
</script>

<div class="content">
	<Bar bind:activeId {single} />
	{#each Array.from({ length: 6 }, (_, i) => i) as i}
		{#if activeId == i.toString()}
			{#if +activeId % 2 == 0}
				<Content2 />
			{:else}
				<Content />
			{/if}
		{/if}
	{/each}
</div>

<style>
	.content {
		font-family: Arial, Helvetica, sans-serif;
		width: 100%;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}
</style>
