<script lang="ts">
	import Nav from '../components/Nav.svelte';

	export let segment: string;
</script>

<style>
	main {
		position: relative;
		background-color: white;
		padding: 2em;
		box-sizing: border-box;
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>