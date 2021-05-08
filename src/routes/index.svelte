<!-- <Header title="Welcome to Super Rentals"/> -->

<!-- <h1>Welcome to SvelteKit</h1> -->
<!-- <p>Visit <a class="text-blue-600 underline" href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->
<script>
	import Jumbo from '../components/jumbo.svelte';
</script>
<Jumbo>
	<h2 class="mt-6 font-bold text-5xl">Welcome to Super Rentals!</h2>
	<p class="mb-6">We hope you find exactly what you're looking for in a place to stay.</p>

	<a sveltekit:prefetch class="pt-2 pr-10 pl-10 pb-2 text-white bg-blue-600 rounded" href="about">About Us</a>
</Jumbo>
