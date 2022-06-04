<script>
	import './../app.css';

</script>

<div class="items-center justify-around bg-white p-4 shadow sm:flex">
	<a href="/"><div class="text-center text-2xl font-extrabold antialiased">KyokuSBC</div></a>
	<div class="flex items-center justify-center gap-3">
		<a href="/" class="hover:underline">Homepage</a>
		<a href="/shop" class="hover:underline	">Shop</a>
		<a href="/" class="hover:underline">Users</a>
		<a href="/" class="hover:underline">More</a>
	</div>
	<div class="flex items-center justify-center gap-3">
		<a href="/login"
			><div class=" border border-black px-2 py-1 hover:bg-black hover:text-white">Login</div></a
		>
		<a href="/register"
			><div class=" border border-black px-2 py-1 hover:bg-black hover:text-white">Register</div></a
		>
	</div>
</div>

<slot />
