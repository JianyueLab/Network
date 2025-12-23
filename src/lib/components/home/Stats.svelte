<script>
	const stats = [
		{ id: 1, name: 'Points of Presence', value: '10' },
		{ id: 2, name: 'Countries & Regions', value: '5' },
		{ id: 3, name: 'Peering Partners', value: '66+' }
	];
</script>

<div class="py-24 sm:py-32 bg-neutral-800">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<dl class="grid grid-cols-2 gap-x-8 gap-y-16 text-center lg:grid-cols-3">
			{#each stats as stat (stat.id)}
				<div class="mx-auto flex max-w-xs flex-col gap-y-4">
					<dt class="text-base/7 text-gray-400">{stat.name}</dt>
					<dd class="order-first text-3xl font-semibold tracking-tight sm:text-5xl text-white">
						{stat.value}
					</dd>
				</div>
			{/each}
		</dl>
	</div>
</div>
