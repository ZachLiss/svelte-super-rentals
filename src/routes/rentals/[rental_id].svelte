<script context="module">
	const COMMUNITY_CATEGORIES = ['Condo', 'Townhouse', 'Apartment'];

	export async function load({page, fetch, session, context}) {
		let response = await fetch(`/api/rentals/${page.params.rental_id}.json`);
		let { data } = await response.json();

      let { id, attributes } = data;
      let type;

      if (COMMUNITY_CATEGORIES.includes(attributes.category)) {
        type = 'Community';
      } else {
        type = 'Standalone';
      }

     let result = { id, type, ...attributes };

    return {
			props: {
				model: result
			}
		}

	}
</script>

<script>
	import Detailed from '$lib/components/rental/detailed.svelte';
	export let model;
</script>

<Detailed rental={model} />
