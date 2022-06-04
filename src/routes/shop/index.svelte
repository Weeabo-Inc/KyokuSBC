<script>
	import PrimaryButton from '$lib/primary-button.svelte';
	import ShopItem from '$lib/shop-item.svelte';
	import { onMount } from 'svelte';
	import { writable } from 'svelte/store';
	/**
	 * @type {any}
	 */
	let data = writable([]);
	let json = import('./data.json').then((JData) => {
		console.log(JData.default);
		data.set(JData.default);
	});
</script>

<div class="p-3 sm:flex items-center justify-center gap-1">
	<PrimaryButton>Auctions</PrimaryButton>
	<PrimaryButton>Categories</PrimaryButton>
	<div class="flex items-center justify-center">
		<input
			type="text"
			class="secondary rounded-l h-fit p-[6px] outline-none w-64"
			placeholder="Item name or 'price:20, name:cool"
		/>
		<div class="primary p-[6px] rounded-r"><i class="fa-solid fa-magnifying-glass" /></div>
	</div>
</div>
<div class="container  mt-5 grid sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-6 gap-5  mx-auto">
	{#each $data as item}
		<ShopItem title={item.AssetName} price={item.Price} rare={item.Limited} id={item.AssetID} />
	{/each}
</div>
