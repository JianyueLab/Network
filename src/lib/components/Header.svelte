<script lang="ts">
	const navItems = [
		{ name: 'HOME', href: '/' },
		{ name: 'BGP.TOOLS', href: 'https://jianyuelab.net' },
		{ name: 'COMPANY', href: 'https://jianyuelab.co' }
	];
</script>

<header>
	<nav
		aria-label="Global"
		class="relative mx-auto flex max-w-7xl items-center justify-between p-6 text-amber-600 lg:px-8"
	>
		<div class="flex lg:flex-1">
			<a href="/" class="-m-1.5 p-1.5 flex">
				<span class="sr-only">JianyueLab Ltd.</span>
				<img src="/logo.png" alt="" class="h-8 w-auto" />
			</a>
		</div>
		<div class="top-full right-4 lg:flex lg:gap-x-12">
			{#each navItems as item (item.href)}
				<a href={item.href} class="text-sm/6 font-semibold">{item.name}</a>
			{/each}
		</div>
	</nav>
</header>
