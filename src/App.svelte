<script lang="ts">
	import Home from './Home.svelte'
	import Room from './Room.svelte'

	let room = window.location.search.slice(1)
</script>

<main>
	{#if room}
	<Room></Room>
	{:else}
	<Home></Home>
	{/if}

</main>

<style>
	:global(body) {
		box-sizing: border-box;
		background-color: #212121;
		color: #a6a28c;
		margin: 0;
		padding: 0;
	}

</style>