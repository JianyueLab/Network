<script lang="ts">
	import './layout.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="https://oss.1n.hk/image/jl/favicon.png" />
</svelte:head>

{@render children()}
