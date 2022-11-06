<script>
	import '../app.css'
	import {
		faHouse,
		faMagnifyingGlass,
		faCartShopping,
		faUser,
	} from '@fortawesome/free-solid-svg-icons'
	import TabItem from './TabItem.svelte'
</script>

<div class="min-h-screen">
	<slot />
	<nav class="py-2 fixed bottom-0 flex w-full text-center">
		<TabItem href="/" icon={faHouse} text="首頁" />
		<TabItem href="/explore" icon={faMagnifyingGlass} text="瀏覽" />
		<TabItem href="/cart" icon={faCartShopping} text="購物車" />
		<TabItem href="/account" icon={faUser} text="帳戶" />
	</nav>
</div>
