<script>
	import { base } from '$app/paths';
</script>

<nav class="h-16 bg-ember-primary menu">

	<a sveltekit:prefetch class="pt-2 pr-10 pl-10 pb-2 text-white inline-block" href="{base}/">
    <h1 class="italic text-3xl pt-4 pr-6">SuperRentals</h1>
	</a>

  <div class="links inline-block">
		<a sveltekit:prefetch class="pt-2 pr-10 pl-10 pb-2 text-white inline-block" href="{base}/about">About</a>
		<a sveltekit:prefetch class="pt-2 pr-10 pl-10 pb-2 text-white inline-block" href="{base}/contact">Contact</a>
  </div>

</nav>
