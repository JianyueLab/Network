<script>
	import { Network, Zap, GraduationCap, Code } from 'lucide-svelte';
	const features = [
		{
			name: 'Multi-Node BGP Infrastructure',
			description:
				'Enterprise-grade BGP routing across Tokyo, Hong Kong, and Johannesburg for optimal traffic management and redundancy.',
			icon: Network
		},
		{
			name: 'Free for Academic & Research',
			description:
				'Complimentary BGP sessions and network services for qualified academic institutions, research organizations, and educational projects supporting innovation and learning.',
			icon: GraduationCap
		}
	];
</script>

<div class="py-24 sm:py-32">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-2xl lg:text-center">
			<h2 class="text-base/7 font-semibold text-amber-600">Why Choose JianyueLab</h2>
			<p class="mt-2 text-4xl font-semibold tracking-tight text-balance sm:text-5xl text-white">
				Professional infrastructure, accessible to everyone
			</p>
			<p class="mt-6 text-lg/8 text-gray-300">
				Enterprise-grade network services with BGP sessions, cloud computing, and LIR capabilities.
				Free access for academic and research institutions.
			</p>
		</div>
		<div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
			<dl
				class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16"
			>
				{#each features as item (item.name)}
					<div class="relative pl-16">
						<dt class="text-base/7 font-semibold text-white">
							<div
								class="absolute top-0 left-0 flex size-10 items-center justify-center rounded-lg bg-gradient-to-br from-amber-600 to-amber-500 shadow-lg"
							>
								<item.icon aria-hidden="true" class="size-6 text-white" />
							</div>
							{item.name}
						</dt>
						<dd class="mt-2 text-base/7 text-gray-400">{item.description}</dd>
					</div>
				{/each}
			</dl>
		</div>
	</div>
</div>
