<template>
	<section>
		<h2>{{ title }}</h2>
		<Article
			v-for="child in children"
			:key="child.title"
			:title="child.title"
			:description="child.description"
			:code="child.code"
			:live="child.live"
			:lang="child.lang"
			:mobile-friendly="child.mobileFriendly"
		/>

		<hr>
		
	</section>
</template>

<script>
	import Article from './Article.vue';

	export default {
		name: 'Section',
		components: {
			Article
		},
		props: {
			title: {
				type: String,
				required: true
			},
			children: {
				type: Array
			},
		}
	}
</script>

<style lang="scss">
  h2 {
      font-size: 1.8em;
      font-weight: 400;
      margin: 1em 0 .5em;
    }

</style>