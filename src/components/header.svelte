<script>
	export let title;
</script>

<div class="jumbo">
  <div class="right tomster"></div>
  <h2>{title}</h2>
	<slot name="body"></slot>
	<slot name="button"></slot>
</div>
