<script>
	export let src, alt;
	let isLarge = false;

	function toggleSize() {
   isLarge = !isLarge;
  }
</script>

<button type="button"
				class="flex-grow-0 w-40 my-5 mx-6 text-center image focus:outline-none"
				class:w-full="{isLarge}"
				on:click={toggleSize}>

  <img {src} {alt} class="rounded">
	<small>View {isLarge ? "Smaller" : "Larger"}</small>
</button>
