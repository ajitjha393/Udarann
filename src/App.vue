<template>
	<div class="container">
		<udarann-new-quote @quoteAdded="newQuote"></udarann-new-quote>
		<udarann-quote-grid :quotes="quotes"></udarann-quote-grid>
		<div class="row">
			<div class="col-sm-12 text-center">
				<div class="alert alert-info">Info: Click on a Quote for deleting it !</div>
			</div>
		</div>
	</div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'

// Quote Limit 10

export default {
	data: function () {
		return {
			maxQuotes: 10,
			quotes: ['Here is a lovely Quote !'],
		}
	},
	methods: {
		newQuote(quote) {
			this.quotes.push(quote)
		},
	},
	components: {
		'udarann-quote-grid': QuoteGrid,
		'udarann-new-quote': NewQuote,
	},
}
</script>

<style></style>
