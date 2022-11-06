<script>
	import '../app.css'
	import {
		faHouse,
		faMagnifyingGlass,
		faCartShopping,
		faUser,
	} from '@fortawesome/free-solid-svg-icons'
	import TabItem from './TabItem.svelte'
	import { page } from '$app/stores'
</script>

<div class="min-h-screen">
	<slot />
	<nav class="py-2 fixed bottom-0 flex w-full text-center">
		<TabItem
			href="/"
			icon={faHouse}
			text="首頁"
			active={['/', '/takeout'].some((path) => path === $page.url.pathname)}
		/>
		<TabItem
			href="/explore"
			icon={faMagnifyingGlass}
			text="瀏覽"
			active={['/explore'].some((path) => path === $page.url.pathname)}
		/>
		<TabItem
			href="/cart"
			icon={faCartShopping}
			text="購物車"
			active={['/cart'].some((path) => path === $page.url.pathname)}
		/>
		<TabItem
			href="/account"
			icon={faUser}
			text="帳戶"
			active={['/account'].some((path) => path === $page.url.pathname)}
		/>
	</nav>
</div>
