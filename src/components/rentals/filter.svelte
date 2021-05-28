<script>
	export let rentals, query;

	$: filteredRentals = rentals.filter((rental) => rental.title.includes(query));
</script>

<slot {filteredRentals}></slot>
