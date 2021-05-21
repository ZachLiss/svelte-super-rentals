<script>
	import { onMount } from 'svelte';

	export let shareURL, attributes, text, hashtags, via;

	const TWEET_INTENT = 'https://twitter.com/intent/tweet'

	onMount(() => {
		currentURL = window.location.href
	});

	$: currentURL = '';

	$: {
    let url = new URL(TWEET_INTENT);

    url.searchParams.set('url', currentURL);

    if (text) {
      url.searchParams.set('text', text);
    }

    if (hashtags) {
      url.searchParams.set('hashtags', hashtags);
    }

    if (via) {
      url.searchParams.set('via', via);
    }

    shareURL = url;
  }

</script>

<a
  {...attributes}
  href={shareURL}
  target="_blank"
  rel="external nofollow noopener noreferrer"
  class="share button pt-2 pr-10 pl-10 pb-2 text-white bg-blue-600 rounded"
>
	<slot></slot>
</a>
