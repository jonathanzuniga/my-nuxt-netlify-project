
<template>
	<article>
		<h1>{{ title }}</h1>

		<vue-markdown>{{ body }}</vue-markdown>
	</article>
</template>

<script>

	import VueMarkdown from 'vue-markdown';

	export default {

		components: {
			VueMarkdown
		},

		async asyncData() {

			let post = await import( '~/content/about/about.json' );

			return post;

		}

	};

</script>
