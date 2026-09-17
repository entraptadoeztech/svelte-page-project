<script lang="ts">
	import '../styles/global.css';
</script>

<svelte:window
	on:sveltekit:navigation-start={() => {
		$navigationState = 'loading';
	}}
	on:sveltekit:navigation-end={() => {
		$navigationState = 'loaded';
	}}
/>

{#if $navigationState === 'loading'}
	<div out:fade={{ delay: 500 }}>
		<PageLoader />
	</div>
{/if}

<slot />
