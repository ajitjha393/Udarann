<template>
	<div class="container">
		<udarann-header></udarann-header>
		<udarann-new-quote @quoteAdded="newQuote"></udarann-new-quote>
		<udarann-quote-grid
			:quotes="quotes"
			@quoteDeleted="deleteQuote"
		></udarann-quote-grid>
		<div class="row">
			<div class="col-sm-12 text-center">
				<div class="alert alert-info">
					Info: Click on a Quote for deleting it !
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
import Header from './components/Header.vue'

// Quote Limit 10

export default {
	data: function() {
		return {
			maxQuotes: 10,
			quotes: ['Here is a lovely Quote !']
		}
	},
	methods: {
		newQuote(quote) {
			this.quotes.push(quote)
		},

		deleteQuote(index) {
			this.quotes.splice(index, 1)
		}
	},

	components: {
		'udarann-quote-grid': QuoteGrid,
		'udarann-new-quote': NewQuote,
		'udarann-header': Header
	}
}
</script>

<style></style>
