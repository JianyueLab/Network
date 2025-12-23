<script>
	import { Github, Linkedin } from 'lucide-svelte';
	const Year = new Date().getFullYear();
	const socials = [
		{ name: 'GitHub', link: 'https://github.com/jianyuelab', icon: Github },
		{ name: 'Linkedin', link: 'https://www.linkedin.com/company/jianyuelab', icon: Linkedin }
	];
</script>

<footer>
	<div
		class="mx-auto mt-16 max-w-7xl px-6 py-12 md:flex md:items-center md:justify-between lg:px-8"
	>
		<div class="flex justify-center gap-x-6 md:order-2">
			{#each socials as item (item.link)}
				<a href={item.link}>
					<span class="sr-only">{item.name}</span>
					<svelte:component
						this={item.icon}
						class="text-neutral-400 transition duration-300 hover:text-neutral-300"
					/>
				</a>
			{/each}
		</div>
		<p class="mt-8 text-left text-sm/6 md:order-1 md:mt-0">
			&copy; {Year} JianyueLab Ltd. All rights reserved. <br />Registered in England and Wales under
			company number 16913067.
		</p>
	</div>
</footer>
