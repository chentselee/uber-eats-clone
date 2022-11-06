<script lang="ts">
	import { page } from '$app/stores'
	export let href: HTMLAnchorElement['href']
	export let text: string
</script>

<a
	{href}
	class={`px-3 py-1.5 rounded-full ${
		$page.url.pathname === href ? 'bg-black text-white' : ''
	}`}>{text}</a
>
