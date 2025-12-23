<script lang="ts">
	import './layout.css';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<title>Network | JianyueLab</title>
	<meta charset="utf-8" />
	<link rel="icon" href="https://oss.1n.hk/image/jl/favicon.png" />
</svelte:head>

<Header />
{@render children()}
<Footer />
