<script lang="ts">
	import { onMount } from 'svelte';
	// import byte1 from '$lib/assets/byte1.jpg';

	// let { children } = $props();

	function openGrokWithText(query: string) {
		const encodedText = encodeURIComponent(query);
		const grokUrl = `https://x.com/i/grok?text=${encodedText}`;
		window.location.href = grokUrl;
	}

	onMount(() => {
		openGrokWithText('Woof, let me talk to Byte.');
	});
</script>

<!-- <h1>Chat with Byte, the AI dog.</h1> -->
<!-- <img src={byte1} alt="Byte" /> -->
