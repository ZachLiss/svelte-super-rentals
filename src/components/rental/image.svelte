<script>
	export let src, alt, detailed;
	let isLarge = false;

	function toggleSize() {
   isLarge = !isLarge;
  }
</script>

<button type="button"
				class="flex-grow-0 my-5 mx-6 text-center image focus:outline-none"
				class:w-full="{isLarge}"
				class:w-40="{!detailed}"
				class:w-80="{detailed}"
				on:click={toggleSize}>

  <img {src} {alt} class="rounded">
	<small class="text-blue-600">View {isLarge ? "Smaller" : "Larger"}</small>
</button>
