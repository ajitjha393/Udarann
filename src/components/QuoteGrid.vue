<template>
	<div class="row">
		<udarann-quote
			v-for="(q,index) in quotes"
			:key="Math.random() + q"
			@click.native="deleteQuote(index)"
		>{{ q }}</udarann-quote>
	</div>
</template>

<script>
import Quote from './Quote.vue'

export default {
	props: ['quotes'],
	methods: {
		deleteQuote(index) {
			this.$emit('quoteDeleted', index)
		},
	},
	components: {
		'udarann-quote': Quote,
	},
}
</script>

<style scoped></style>
