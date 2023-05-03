<template>
	<div id="app">
		<app-header />
		<section class="container">
			<app-grid />
			<app-form />
		</section>
	</div>
</template>

<script>
import AppGrid from './components/AppGrid.vue'
import AppForm from './components/AppForm.vue'

export default {
	components: {
		AppGrid,
		AppForm,
	},
	created() {
		this.$store.commit('initialArrIndex', window.location.search)
	},
}
</script>

<style lang="scss">
#app {
	margin: 5vmin 5vmin 0;
}

.container {
	display: flex;
	flex-direction: column;
}
</style>
