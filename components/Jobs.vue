<template>
	
	<div class="jobs">
		<p>{{ job }}</p>
	</div>
	
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
	props: ['job']
})
</script>

<style lang="scss" scoped>
.jobs {
	padding: 1rem;
}
</style>
