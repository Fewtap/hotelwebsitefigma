<script>
	import Navbar from './components/navbar.svelte';
	import Section1 from './components/section1.svelte';
	import Section2 from './components/section2.svelte';
	import Section3 from './components/section3.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		//print the width of the screen
		console.log(window.innerWidth);
	});
</script>

<Section1 />

<Section3 />
