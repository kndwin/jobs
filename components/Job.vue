<template>
	<div class="job">
		<h2>
			<a v-bind:href=job.link>
				{{ job.title }}
			</a>
		</h2>
		<p>{{ job.timePosted }}</p>
		<p>{{ job.company }}</p>
		<p>{{ job.source }}</p>
	</div>
</template>

<script lang="ts">
	import Vue from 'vue'
	export default Vue.extend({
		props: ['job', 'id']	
	})
</script>

<style lang="scss" scoped>
	.job {
		padding: 1rem;
	}
</style>
