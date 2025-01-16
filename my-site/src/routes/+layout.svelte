<script lang="ts">
	import '../app.css';
	import Navbar from '../components/navbar.svelte';
	let { children } = $props();
</script>

<main>
	{@render children()}
</main>

<footer>

</footer>
