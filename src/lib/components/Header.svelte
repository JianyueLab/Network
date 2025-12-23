<script lang="ts">
	import { Menu, X } from 'lucide-svelte';

	let mobileMenuOpen = false;

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

		<!-- Desktop Navigation -->
		<div class="hidden lg:flex lg:gap-x-12">
			{#each navItems as item (item.href)}
				<a href={item.href} class="text-sm/6 font-semibold">{item.name}</a>
			{/each}
		</div>

		<!-- Mobile Menu Button -->
		<div class="flex lg:hidden">
			<button
				type="button"
				class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5"
				on:click={() => (mobileMenuOpen = !mobileMenuOpen)}
			>
				<span class="sr-only">Open main menu</span>
				{#if mobileMenuOpen}
					<X class="h-6 w-6" aria-hidden="true" />
				{:else}
					<Menu class="h-6 w-6" aria-hidden="true" />
				{/if}
			</button>
		</div>
	</nav>

	<!-- Mobile Menu -->
	{#if mobileMenuOpen}
		<div class="lg:hidden">
			<div class="space-y-1 px-6 pb-6 pt-2">
				{#each navItems as item (item.href)}
					<a
						href={item.href}
						class="block rounded-lg px-3 py-2 text-base font-semibold text-amber-600 hover:bg-amber-50"
						on:click={() => (mobileMenuOpen = false)}
					>
						{item.name}
					</a>
				{/each}
			</div>
		</div>
	{/if}
</header>
