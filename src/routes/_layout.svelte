<script lang="ts">
	import Nav from '../components/Nav.svelte';

	export let segment: string;
</script>

<style global lang="scss">
	@import "../main.scss";
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>