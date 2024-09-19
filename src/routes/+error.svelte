<script>
	import { page } from '$app/stores';
</script>

<div class="flex items-center justify-center h-screen">
    <span class="text-white font-mono">
        {#if $page.status === 404}
            <h1>Page not found</h1>
            <p>Click <a href="/" class="underline">here</a> to return to the homepage.</p>
        {:else}
            <h1>An unexpected error occured.</h1>
            <p>Error code: {$page.status}</p>
        {/if}
        
    </span>
</div>

<!-- {#if status === 404}
	<div class="flex items-center justify-center h-screen">
		<span class="text-white">
			<h1 class="font-mono text-center">404!</h1>
			<p class="font-mono">The page you're looking for could not be found.</p>
		</span>
	</div>
{:else}
	<div class="flex items-center justify-center h-screen">
		<span class="text-white">
			<h1 class="font-mono text-center">Error {status}!</h1>
			<p class="font-mono">{message}</p>
		</span>
	</div>
{/if} -->
