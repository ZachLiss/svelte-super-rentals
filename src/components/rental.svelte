<script>
	import Image from '../components/rental/image.svelte';
	import Map from '../components/map.svelte';
</script>
<article class="mt-4 bg-gray-100 hover:bg-gray-200 py-5 px-6 flex flex-wrap justify-between items-center  rental">
	<Image
		src="https://upload.wikimedia.org/wikipedia/commons/c/cb/Crane_estate_(5).jpg"
    alt="A picture of Grand Old Mansion"
		class="test"
		/>
  <div class="flex flex-wrap align-around justify-between flex-grow h-40 my-5 mx-6  details">
    <h3 class="text-blue-600 font-bold w-full">Grand Old Mansion</h3>
    <div class="w-1/2 italic font-light whitespace-nowrap detail owner">
      <span class="not-italic font-normal">Owner:</span> Veruca Salt
    </div>
    <div class="w-1/2 italic font-light whitespace-nowrap detail type">
      <span class="not-italic font-normal">Type:</span> Standalone
    </div>
    <div class="w-1/2 italic font-light whitespace-nowrap detail location">
      <span class="not-italic font-normal">Location:</span> San Francisco
    </div>
    <div class="w-1/2 italic font-light whitespace-nowrap detail bedrooms">
      <span class="not-italic font-normal">Number of bedrooms:</span> 15
    </div>
  </div>

	<Map
		lat="37.7749"
		lng="-122.4194"
		zoom="9"
		width="150"
		height="150"
		alt="A map of Grand Old Mansion"
		/>
</article>
