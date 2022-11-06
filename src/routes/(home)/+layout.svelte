<script lang="ts">
	import TabItem from './TabItem.svelte'
</script>

<nav class="flex justify-center gap-1 mt-3">
	<TabItem href="/" text="外送" />
	<TabItem href="/takeout" text="自取" />
</nav>

<slot />
