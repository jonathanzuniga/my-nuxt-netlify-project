
<template>
	<article>
		<img v-if="thumbnail" :src="thumbnail">

		<h1>{{ title }}</h1>

		<small>{{ date }}</small>

		<p>{{ body }}</p>
	</article>
</template>

<script>

	export default {

		data() {

			return {
				thumbnail: '',
				title: '',
				date: '',
				body: ''
			}

		},

		async asyncData( { params } ) {

			// const postPromise = process.BROWSER_BUILD
			//   ? import('~/content/blog/posts/' + params.slug + '.json')
			//   : Promise.resolve(
			//       require('~/content/blog/posts/' + params.slug + '.json')
			//     );

			let post = await import( '~/content/blog/posts/' + params.slug + '.json' );

			return post;

		}

	};

</script>
