<script>
	import PrimaryButton from './primary-button.svelte';
	import SecondaryButton from './secondary-button.svelte';

	export /**
	 * @type {string}
	 */
	let title;
	export /**
	 * @type {number}
	 */
	let price;
	export /**
	 * @type {boolean}
	 */
	let rare;

	/**
	 * @type {number}
	 */
	export let id;
</script>

<a href="/shop/{id}">
	<div class=" overlay h-[450px] transition-all duration-300  relative w-full   shadow-xl ">
		<img
			src="https://polytoria.com/assets/thumbnails/catalog/15075.png?v=1"
			class="object-cover  bg-zinc-900 w-full h-2/4"
			alt=""
		/>
		<div class="p-2">
			<div class="text-3xl font-bold ">{title}</div>
			<div class="">By <span class="link">Owner</span></div>
			<div class="flex gap-4">
				{#if rare}
					<div
						class="w-max text-sm p-0.5 bg-gradient-to-r from-red-500 font-bold to-yellow-500 text-white"
					>
						LIMITED
					</div>
				{/if}
				<div class="font-bold text-green-600">
					{price}
					<li class="fa fa-dollar" />
				</div>
			</div>
		</div>
		<div class="text-center grid grid-cols-2 -gap-6 absolute bottom-2 w-full ">
			<PrimaryButton>Buy</PrimaryButton><SecondaryButton>Wishlist</SecondaryButton>
		</div>
	</div>
</a>
