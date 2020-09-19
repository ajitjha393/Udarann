<template>
	<div class="row">
		<udarann-quote v-for="q in quotes" :key="Math.random() + q">
			{{ q }}
		</udarann-quote>
	</div>
</template>

<script>
import Quote from './Quote.vue'

export default {
	props: ['quotes'],
	components: {
		'udarann-quote': Quote
	}
}
</script>

<style scoped></style>
