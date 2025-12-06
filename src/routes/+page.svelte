<script>
	const ix = [
		{ id: 3911, name: "BGP.Exchange", location: "Tokyo, Japan"}
	]

	const upstream = [
		{ name: 'Liu HaoRan', asn: 213605 },
		{ name: 'The Constant Company, LLC', asn: 20473 },
		{ name: 'MoeDove LLC', asn: 44324 }
	];
</script>

<svelte:head>
	<title>Network | JianyueLab</title>
	<meta charset="utf-8" />
</svelte:head>

<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 my-16">
	<div class="mx-auto max-w-3xl">
		<h1 class="text-center text-4xl">AS 215172 | JianyueLab Network</h1>

		<h2 class="mt-4 text-2xl">Introduction</h2>
		<p>
			<a href="https://bgp.tools/as/215172" class="underline">AS 215172</a> is operated by
			<a href="https://jhl.hk" class="underline">Jianyue Hugo Liang</a>, for learning and testing purpose.
		</p>
		<p>
			<a href="https://bgp.tools/as/203168" class="underline">AS 203168</a> is operated by
			<a href="https://jhl.hk" class="underline">Janyue Aosugi</a>, for business purpose.
		</p>

		<h2 class="mt-4 text-2xl">Locations</h2>
		<ul class="list-disc">
			<li>Tokyo, Japan (Open to Peer)</li>
			<li>Osaka, Japan</li>
			<li>Kobe, Japan (Open to Peer)</li>
			<li>Frankfurt, Germany</li>
		</ul>

		<h2 class="mt-4 text-2xl">Peer</h2>
		<p>We have an open peering policy. You can peer with us through Internet eXchanges that we have in common, or individually.</p>

		<h2 class="mt-4 text-2xl">Internet Exchange (IX)</h2>
		<ul class="list-disc">
			{#each ix as item (item.id)}
				<li><a href="https://www.peeringdb.com/ix/{item.id}" class="underline">{item.name} | {item.location}</a></li>
			{/each}
		</ul>

		<h2 class="mt-4 text-2xl">Upstreams</h2>
		<ul class="list-disc">
			{#each upstream as item (item.asn)}
				<li><a href="https://bgp.tools/as/{item.asn}" class="underline">{item.name} (AS {item.asn})</a></li>
			{/each}
		</ul>

		<h2 class="mt-4 text-2xl">Links</h2>
		<ul class="list-disc">
			<li><a href="https://jhl.hk" class="underline">Profile Page</a></li>
			<li><a href="https://article.jhl.idv.hk" class="underline">Blogs</a></li>
			<li><a href="https://jianyuelab.org" class="underline">JianyueLab</a></li>
		</ul>

		<footer class="my-4">
			<p>Last Updated: 28-11-2025. IPv6 Supported.</p>
		</footer>
	</div>
</div>
