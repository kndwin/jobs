<template>
	<div class="job">
		<h2 class="title">
			<a v-bind:href=job.link>
				{{ job.title }}
			</a>
		</h2>
		<p class="company">🏢 {{ job.company }}</p>
		<p class="timePosted">⌚ {{ job.timePosted }}</p>
		<p class="source">{{ job.source }}</p>
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
  border: 1px solid black;
  border-radius: 5px; 
  margin: 0.5rem;
  height: 15rem;
}
.source {
  padding: 0.5rem;
  font-weight: bold;
  background-color: #efefef;
  width: fit-content;
  border-radius: 5px;
}
.company {
  font-size: 14pt;
  font-weight: bold;
}
.title {
  a {
    text-decoration: none;
    font-size: 14pt;
    color: black;
  }
}
</style>
