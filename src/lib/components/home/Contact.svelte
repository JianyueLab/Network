<script>
	const contact = [
		{ name: 'NOC / Peering', address: 'noc@jianyuelab.net' },
		{ name: 'Abuse Contact', address: 'abuse@jianyuelab.net' }
	];
</script>

<div class="py-8 sm:py-16" id="contact">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div
			class="mx-auto max-w-2xl divide-y divide-neutral-100 lg:mx-0 lg:max-w-none dark:divide-white/10"
		>
			<div class="grid grid-cols-1 gap-10 py-16 lg:grid-cols-3">
				<div>
					<h2 class="text-4xl font-semibold tracking-tight text-pretty text-white">Get in touch</h2>
					<p class="mt-4 text-base/7 text-neutral-400">
						Our network operations team is available 24/7 to assist with peering requests, technical
						inquiries, and network abuse reports.
					</p>
				</div>
				<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:col-span-2 lg:gap-8">
					{#each contact as item (item.address)}
						<div class="rounded-2xl p-10 bg-neutral-800/50">
							<h3 class="text-base/7 font-semibold text-white">{item.name}</h3>
							<dl class="mt-3 space-y-1 text-sm/6 text-gray-400">
								<div>
									<dt class="sr-only">Email</dt>
									<dd>
										<a
											href="mailto:{item.address}"
											class="font-semibold text-amber-600 hover:text-amber-500 transition-colors"
										>
											{item.address}
										</a>
									</dd>
								</div>
							</dl>
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</div>
