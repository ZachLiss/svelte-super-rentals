<script>
	export let lat, lng, zoom, width, height;
	export let alt = `Map image at coordinates ${lat},${lng}`


	let token = encodeURIComponent(import.meta.env.VITE_MAPBOX_TOKEN);

	$: src=`https://api.mapbox.com/styles/v1/mapbox/streets-v11/static/${lng},${lat},${zoom}/${width}x${height}@2x?access_token=${token}`
</script>

<div class="map">
  <img
    alt={alt}
		src={src}
    width={width} height={height}
		class="rounded"
  >
</div>
