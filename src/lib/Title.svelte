<script lang="ts">
	import { page } from '$app/stores';
    import { pages } from '$lib/index';

    let title: string;

    $: path = $page.url.pathname;

    $: {
        const normalized = path.endsWith('/') && path !== '/' ? path.slice(0, -1) : path;
        const match = pages.find((p) => p.path === normalized);
        title = match ? `operfesium -- ${match.name}` : 'operfesium';
    }
</script>

<svelte:head>
    <title>{title}</title>
</svelte:head>

