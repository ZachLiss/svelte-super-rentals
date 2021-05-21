<script>
	import Jumbo from '$lib/components/jumbo.svelte';
	import Image from '$lib/components/rental/image.svelte';
	import Map from '$lib/components/map.svelte';
	import ShareButton from '$lib/components/share-button.svelte';

	export let rental;
</script>

<Jumbo>
  <h2 class="mt-6 font-bold text-5xl">{rental.title}</h2>
  <p class="mb-6">Nice find! This looks like a nice place to stay near {rental.city}.</p>

	<ShareButton
		text="Check out {rental.title} on Super Rentals!"
		hashtags="vacation,travel,authentic,blessed,superrentals"
		via="emberjs">
    Share on Twitter
	</ShareButton>
</Jumbo>

<article class="mt-4 py-5 px-6 flex flex-wrap justify-center items-start rental detailed">
  <Image
    src={rental.image}
    alt="A picture of {rental.title}"
		detailed
  />

  <div class="flex flex-col align-around justify-between flex-grow h-40 my-5 mx-6 w-1/2 details">
    <h3 class="text-3xl mb-2.5 font-bold w-full">About {rental.title}</h3>

    <div class="my-1 italic font-light whitespace-nowrap detail owner">
      <span class="not-italic font-normal">Owner:</span> {rental.owner}
    </div>
    <div class="my-1 italic font-light whitespace-nowrap detail type">
      <span class="not-italic font-normal">Type:</span> {rental.type}
    </div>
    <div class="my-1 italic font-light whitespace-nowrap detail location">
      <span class="not-italic font-normal">Location:</span> {rental.city}
    </div>
    <div class="my-1 italic font-light whitespace-nowrap detail bedrooms">
      <span class="not-italic font-normal">Number of bedrooms:</span> {rental.bedrooms}
    </div>

    <div class="my-1 italic font-light detail description">
      <p>{rental.description}</p>
    </div>
  </div>

  <Map
    lat={rental.location.lat}
    lng={rental.location.lng}
    zoom="12"
    width="894"
    height="600"
    alt="A map of {rental.title}"
    class="large"
  />
</article>
