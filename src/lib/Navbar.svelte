<script lang="ts">
	import { page } from '$app/stores';
    import { pages } from '$lib/index';

	$: path = $page.url.pathname;
</script>

{#each pages as p, i}
	{#if p.path === path}
		{p.name}
	{:else}
		<a href={p.path}>{p.name}</a>
	{/if}
	{#if i < pages.length - 1} |&nbsp;{/if}
{/each}

