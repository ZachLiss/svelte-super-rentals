<script>
	import Jumbo from '../components/jumbo.svelte';
</script>

<Jumbo>
  <h2 class="mt-6 font-bold text-5xl">About Super Rentals</h2>
  <p class="mb-6">
    The Super Rentals website is a delightful project created to explore Ember.
    By building a property rental site, we can simultaneously imagine traveling
    AND building Ember applications.
  </p>

	<a sveltekit:prefetch class="pt-2 pr-10 pl-10 pb-2 text-white bg-blue-600 rounded" href="contact">Contact Us</a>
</Jumbo>
