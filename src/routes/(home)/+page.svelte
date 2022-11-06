<script lang="ts">
	import Fa from 'svelte-fa'
	import {
		faMagnifyingGlass,
		faSliders,
		faArrowLeft,
	} from '@fortawesome/free-solid-svg-icons'
	let isInputFocused = false
</script>

<div class="text-lg text-center mt-4 font-semibold">現在．敦化南路一段2號</div>
<div
	class="mx-3.5 mt-3 px-4 py-2 bg-gray-200 flex items-center rounded-full text-lg"
>
	<div>
		<Fa
			icon={isInputFocused ? faArrowLeft : faMagnifyingGlass}
			class="w-[18px]"
		/>
	</div>
	<input
		type="text"
		placeholder="美食、生鮮雜貨、飲料等。"
		class="grow ml-3 bg-inherit text-base font-semibold placeholder:text-gray-600 placeholder:font-semibold"
		on:focusin={() => (isInputFocused = true)}
		on:focusout={() => (isInputFocused = false)}
	/>
	<span class="w-[1px] h-7 self-stretch bg-gray-300" />
	<Fa icon={faSliders} class="ml-2" />
</div>
