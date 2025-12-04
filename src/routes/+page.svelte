<script>
	const upstream = [
		{ name: 'Liu HaoRan', asn: 213605 },
		{ name: 'The Constant Company, LLC', asn: 20473 },
		{ name: 'MoeDove LLC', asn: 44324 }
	];

	const peer = [
		{ name: 'Liu HaoRan', asn: 213605 },
		{ name: 'The Constant Company, LLC', asn: 20473 },
		{ name: 'MoeDove LLC', asn: 44324 },
		{ name: 'Rui Feng', asn: 211575 },
		{ name: 'Liu HaoRan', asn: 154185 },
		{ name: 'Yijia Xu', asn: 210352 }
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
			<a href="#" class="underline">Waiting for ASN Assignment</a> is operated by
			<a href="https://jhl.hk" class="underline">Jianyue Hugo Liang</a>, for business purpose.
		</p>

		<h2 class="mt-4 text-2xl">Locations</h2>
		<ul class="list-disc">
			<li>Tokyo, Japan</li>
			<li>Osaka, Japan</li>
			<li>Frankfurt, Germany</li>
		</ul>

		<h2 class="mt-4 text-2xl">Upstreams</h2>
		<ul class="list-disc">
			{#each upstream as item (item.asn)}
				<li><a href="https://bgp.tools/as/{item.asn}" class="underline">{item.name} (AS {item.asn})</a></li>
			{/each}
		</ul>

		<h2 class="mt-4 text-2xl">Peers</h2>
		<ul class="list-disc">
			{#each peer as item (item.asn)}
				<li><a href="https://bgp.tools/as/{item.asn}" class="underline">{item.name} (AS {item.asn})</a></li>
			{/each}
		</ul>

		<h2 class="mt-4 text-2xl">Links</h2>
		<ul class="list-disc">
			<li><a href="https://jhl.hk" class="underline">Profile Page</a></li>
			<li><a href="https://article.jhl.idv.hk" class="underline">Blogs</a></li>
			<li><a href="https://jianyuelab.org" class="underline">JianyueLab</a></li>
		</ul>

		<h2 class="mt-4 text-2xl">Connectivity</h2>
		<img src="https://bgp.tools/pathimg/215172-default?" alt="BGP Connectivity Map" class="w-auto" />

		<footer class="my-4">
			<p>Last Updated: 28-11-2025. IPv6 Supported.</p>
		</footer>
	</div>
</div>
