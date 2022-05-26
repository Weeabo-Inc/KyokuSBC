<script>
	import PrimaryButton from './primary-button.svelte';

	// @ts-ignore
	export let title;
	export let price;
	export let rare;
</script>

<div
	class=" overlay  transition-all duration-300 hover:scale-110 relative w-full rounded  shadow-xl "
>
	<img
		src="https://polytoria.com/assets/thumbnails/catalog/15075.png?v=1"
		class="object-cover rounded-t rounded-b-xl bg-zinc-900 w-full h-2/4"
		alt=""
	/>
	<div class="p-2">
		<div class="text-3xl font-bold ">{title}</div>
		<div class="">By <span class="link">Owner</span></div>
		<div class="flex gap-4">
        {#if rare}
			<div class="w-max rounded text-sm p-0.5 bg-yellow-500 text-white">LIMITED</div>
		{/if}
		<div class="font-bold text-green-600">
			{price}
			<li class="fa fa-dollar" />
		</div>
    </div>
	</div>
	<a href="/buy/1" class="text-center absolute bottom-2 w-full "
		><PrimaryButton>Buy</PrimaryButton></a
	>
</div>
