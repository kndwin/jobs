<template>
	<div class="job">
		<h2 class="title">
			<a v-bind:href=job.link>
				{{ job.title }}
			</a>
		</h2>
		<div class="companyAndTimePostedWrapper">
			<img class="icon"
				alt="Icon of building"
				src="https://img.icons8.com/ios/50/000000/building.png"/>
			<p class="company">
				{{ job.company }}
			</p>
			<p class="timePosted">
				{{ job.timePosted }}
			</p>
		</div>
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

.timePosted {
	color: #666;
}

.companyAndTimePostedWrapper {
	display: flex;
	align-items: baseline;
	overflow: hidden; 

	p {
		margin: 0 1rem 0 0;
	}
	
}

.title {
  a {
    text-decoration: none;
    font-size: 14pt;
    color: black;
  }
}

.icon {
	height: 1em;
	margin: 0 0.2rem 0 0; 
}

@media (width: 700px) {
	.companyAndTimePostedWrapper {
		display: block;
	}
}

</style>
