<template>
		<article>
				<h3>{{ title }} <span class="lang">({{ lang }})</span></h3>
				<p>{{ description }}</p>
				<!-- <p v-if="mobileFriendly" class="mobile-friendly">try on mobile</p> -->
				<div>
					<a v-if="hasCode"
						:href="code"
						:title="title + ' – code'"
						>[code]</a>

					<a v-if="hasLive"
						:href="live"
						:title="title + ' – live'"
						>[live]</a>
				</div>
			</article>

</template>

<script>
	export default {
		name: 'Article',
		props: ['title', 'description', 'code', 'live', 'lang', 'mobileFriendly'],
		computed: {
			hasCode() {
				return this.code;
			},
			hasLive() {
				return this.live;
			}
		}

	}
</script>

<style lang="scss">
	    
    article {
      display: flex;
      flex-direction: column;
      margin-bottom: 1em;
    }

    h3 {
    	font-size: 1em;
      margin: .5em 0;
    }

    p {
      margin: 0 0 .5em;
    }

    a {
      margin-right: .5em;
    }

	.lang {
		color: #aaa;
		font-size: 1em;
	}

	.mobile-friendly {
		color: lime;
		font-size: 0.8em;
	}
</style>