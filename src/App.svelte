<script lang="ts">
	import Home from './Home.svelte'
	import ChartBox from './ChartBox.svelte'

	let room = window.location.search.slice(1)
</script>

<main>
	{#if room}
	<ChartBox></ChartBox>
	{:else}
	<Home></Home>
	{/if}

</main>

<style>
	

</style>