<script>
	export let todos;
	export let remove;
</script>

<div class="rounded-lg shadow-lg p-8 flex flex-col gap-4">
	<!-- svelte version of .map -->
	{#each todos as item, index}
		<div class="rounded-md p-4 flex flex-row justify-between border-2 border-gray-800">
			<div class="font-medium text-sm">{item.text}</div>
			<button on:click={() => remove(index)}>❌</button>
		</div>
	{/each}
</div>
