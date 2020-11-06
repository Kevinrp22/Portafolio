<script>
	import BigNavbar from "./BigNavbar.svelte";
	import SmallNavbar from "./SmallNavbar.svelte";

	let width;
</script>

<svelte:window bind:innerWidth={width} />
{#if width > 667}
<BigNavbar />
{:else}
<SmallNavbar />
{/if}
