<script lang="ts">
	import '../app.css'
	import Navbar from '$lib/Navbar.svelte';
	import Title from '$lib/Title.svelte';

	let { children } = $props();
</script>

<Title />

<div class="window">
	<div class="titlebar">
		<div class="window-icon">
			<img src="/assets/icons/globe.svg" class="window-icon" alt="globe icon">
		</div>
		<div class="title">operfesium -- <Navbar /></div>
		<div class="window-controls">
			<img src="/assets/icons/window-minimize.svg" class="icon" alt="minimize">
			<img src="/assets/icons/window-maximize.svg" class="icon" alt="maximize">
			<img src="/assets/icons/window-close.svg" class="icon" alt="close">
		</div>
	</div>
	<div class="content">
		<h1>operfesium</h1>
		<p class="mobile-navbar"><Navbar /></p>
		{@render children()}
	</div>
</div>