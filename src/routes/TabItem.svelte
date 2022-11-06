<script lang="ts">
	import Fa from 'svelte-fa'
	import type { IconDefinition } from '@fortawesome/free-solid-svg-icons'
	import { page } from '$app/stores'
	export let icon: IconDefinition
	export let text: string
	export let href: HTMLAnchorElement['href']
</script>

<a
	{href}
	class={`grow flex flex-col items-center gap-1.5 ${
		$page.url.pathname === href ? '' : 'text-gray-500'
	}`}
>
	<Fa {icon} class="text-2xl" />
	<span class="text-xs">{text}</span>
</a>
