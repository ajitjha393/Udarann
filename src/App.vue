<template>
	<div class="container">
		<udarann-quote-grid :quotes="quotes"></udarann-quote-grid>
	</div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'

// Quote Limit 10

export default {
	data: function() {
		return {
			maxQuotes: 10,
			quotes: ['Here is a lovely Quote !']
		}
	},
	components: {
		'udarann-quote-grid': QuoteGrid
	}
}
</script>

<style></style>
