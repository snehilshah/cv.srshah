<script lang="ts">
	import Header from '$lib/Header.svelte';
	import '../app.css';
</script>

<Header />

<main class="pt-12 layout-md">
	<slot />
</main>

