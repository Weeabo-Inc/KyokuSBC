<script>
import PrimaryButton from "$lib/primary-button.svelte";

import ShopItem from "$lib/shop-item.svelte";

</script>
<div class="p-3 flex items-center gap-1">
    <PrimaryButton>Auctions</PrimaryButton>
    <PrimaryButton>Categories</PrimaryButton>
    <div class="flex items-center"><input type="text" class="secondary rounded-l h-fit p-[6px] outline-none w-64" placeholder="Item name or 'price:20, name:cool"><div class="primary p-[6px] rounded-r"><i class="fa-solid fa-magnifying-glass"></i></div></div>
</div>
    <div class="container  mt-5 grid sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-6 gap-5 text-white mx-auto">
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
       <ShopItem/>
    </div>
