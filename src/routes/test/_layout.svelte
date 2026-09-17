<script lang="ts">
	import { fade } from 'svelte/transition';

	import navigationState from '../stores/navigationState';
	import PageLoader from '../components/PageLoader.svelte';
	import 'https://raw.githubusercontent.com/entraptadoeztech/sveltekit-page-progress-demo/refs/heads/main/src/styles/test.css';
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
