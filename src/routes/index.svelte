<script context="module">
	const COMMUNITY_CATEGORIES = ['Condo', 'Townhouse', 'Apartment'];

	export async function load({page, fetch, session, context}) {
		let response = await fetch('/api/rentals.json');
		let { data } = await response.json();

    let result = data.map((model) => {
      let { id, attributes } = model;
      let type;

      if (COMMUNITY_CATEGORIES.includes(attributes.category)) {
        type = 'Community';
      } else {
        type = 'Standalone';
      }

      return { id, type, ...attributes };
    });

    return {
			props: {
				model: result
			}
		}

	}
</script>

<script>
	import Jumbo from '../components/jumbo.svelte';
	import Rentals from '../components/rentals.svelte';

	export let model;
</script>

<Jumbo>
	<h2 class="mt-6 font-bold text-5xl">Welcome to Super Rentals!</h2>
	<p class="mb-6">We hope you find exactly what you're looking for in a place to stay.</p>

	<a sveltekit:prefetch class="pt-2 pr-10 pl-10 pb-2 text-white bg-blue-600 rounded" href="about">About Us</a>
</Jumbo>

<Rentals rentals={model} />
