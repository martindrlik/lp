<script>
	import { page } from '$app/state';
	const isApproved = page.url.searchParams.has('approved');
</script>

<div class="flex h-screen items-center justify-center">
	{#if isApproved}
		Approved
	{:else}
		<a
			href="/?approved"
			data-sveltekit-reload
			class="rounded bg-blue-500 px-4 py-2 font-bold text-white hover:bg-blue-700"
		>
			Approve
		</a>
	{/if}
</div>

<style lang="postcss">
	@reference "tailwindcss";
	:global(html) {
		background-color: theme(--color-gray-100);
	}
</style>
