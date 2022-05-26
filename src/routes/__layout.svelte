<script>
	import Layered from "$lib/svg/layered-peaks-haikei.svg"
	import PrimaryButton from "$lib/primary-button.svelte";
	
	import '../app.css';
import SecondaryButton from "$lib/secondary-button.svelte";
</script>
<svelte:head>
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css">
</svelte:head>
<div
	class="overlay static mx-auto grid grid-cols-1 items-center justify-center gap-2 p-6 shadow-lg sm:flex sm:justify-between md:gap-0"
>
	<div class="items-center justify-center gap-2 sm:flex">
		<a href="/"
			><div
				class="bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-center text-3xl font-extrabold text-transparent"
			>
				Kyoku SBC
			</div></a
		>
		<div class="ml-5 flex items-center justify-center gap-5">
			<a href="/"><div class="hover:underline">Home</div> </a>
			<a href="/shop"><div class="hover:underline">Store</div> </a>
			<a href="/"><div class="hover:underline">Forum</div> </a>
			<a href="/"><div class="hover:underline">More</div> </a>
		</div>
	</div>
	<div class="flex items-center justify-center gap-2">
		<a href="/login"><PrimaryButton>Login</PrimaryButton></a>
		<a href="/register"><SecondaryButton>Register</SecondaryButton></a>
	</div>
</div>
	<slot />

<img src={Layered} class="sticky -z-10 w-screen bottom-0 h-screen object-cover" alt="">
