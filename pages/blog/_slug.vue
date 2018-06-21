
<template>
	<article>
		<img v-if="thumbnail" :src="thumbnail">

		<h1>{{ title }}</h1>

		<small>{{ date }}</small>

		<vue-markdown>{{ body }}</vue-markdown>
	</article>
</template>

<script>

	import VueMarkdown from 'vue-markdown';

	export default {

		components: {
			VueMarkdown
		},

		async asyncData( { params } ) {

			// const postPromise = process.BROWSER_BUILD
			//   ? import('~/content/blog/posts/' + params.slug + '.json')
			//   : Promise.resolve(
			//       require('~/content/blog/posts/' + params.slug + '.json')
			//     );

			let post = await import( '~/content/blog/posts/' + params.slug + '.json' );

			if ( ! post.thumbnail )
				Object.assign( post, { thumbnail: '' } );

			return post;

		}

	};

</script>
