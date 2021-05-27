<script>
	export let rentals, query;

	import Rental from '../components/rental.svelte';

	$: results = rentals.filter((rental) => rental.title.includes(query));
</script>

<div class="rentals">
	<label class="flex flex-col align-center">
    <span class="text-3xl italic font-extralight text-center mt-8 mb-4">Where would you like to stay?</span>
    <input bind:value={query} class=" border border-gray-200 text-2xl p-3 light">
  </label>

  <ul class="results">
		{#each rentals as rental}
			<li class="list-none py-2.5 px-3.5"><Rental {rental}/></li>
		{/each}
  </ul>
</div>
