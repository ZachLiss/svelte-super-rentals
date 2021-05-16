<script>
	import Image from '../components/rental/image.svelte';
	import Map from '../components/map.svelte';

	export let rental;
</script>

<article class="mt-4 bg-gray-100 hover:bg-gray-200 py-5 px-6 flex flex-wrap justify-between items-center  rental">
	<Image
		src={rental.image}
		alt="A picture of {rental.title}"
		class="test"
		/>
  <div class="flex flex-wrap align-around justify-between flex-grow h-40 my-5 mx-6  details">
		<h3 class="text-blue-600 font-bold w-full">
			<a sveltekit:prefetch class="" href="/rentals/{rental.id}">
        {rental.title}
			</a>
    </h3>
    <div class="w-1/2 italic font-light whitespace-nowrap detail owner">
      <span class="not-italic font-normal">Owner:</span> {rental.owner}
    </div>
    <div class="w-1/2 italic font-light whitespace-nowrap detail type">
      <span class="not-italic font-normal">Type:</span> {rental.type}
    </div>
    <div class="w-1/2 italic font-light whitespace-nowrap detail location">
      <span class="not-italic font-normal">Location:</span> {rental.city}
    </div>
    <div class="w-1/2 italic font-light whitespace-nowrap detail bedrooms">
      <span class="not-italic font-normal">Number of bedrooms:</span> {rental.bedrooms}
    </div>
  </div>

	<Map
		lat={rental.location.lat}
		lng={rental.location.lng}
		zoom="9"
		width="150"
		height="150"
		alt="A map of {rental.title}"
		/>
</article>
