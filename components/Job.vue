<template>
	<div class="job">
			<div class="flexRow">
				<span class="source">
					{{ job.source }}
				</span>
		<a v-bind:href=job.link>
				<h2 class="title">
						{{ job.title }}
				</h2>
		</a>
			</div>
		<br>
		<div class="flexRow">
			<img class="icon"
				alt="Icon of building"
				src="https://img.icons8.com/ios/50/000000/building.png"/>
			<p class="company">
				{{ job.company }}
			</p>
			<p  class="timePosted">
				{{ job.timePosted }}
			</p>
		</div>
		<br>
		<a  class="show"
			v-on:click="show = !show">
			<span v-if="!show">
				Show More
			</span>
			<span v-else>
				Hide
			</span>
		</a>
		<div class="descriptionHTML" 
				v-html=job.descriptionHTML 
			 v-if="show"
			>
			Hover
		</div>
	</div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: ['job', 'id'], 
	data() {
		return {
			show: false
		}
	}
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
  padding:  .45em .3em .3em .45em;
	margin: 0 1rem 0 0;
	font-size: 12pt; 
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

.flexRow {
	display: flex;
	align-items: baseline;
	overflow: hidden; 

	p {
		margin: 0 1rem 0 0;
	}
	
}

.title {
	display: flex; 
	align-items: flex-start; 
}

h2 {
	padding: 0.3em 0 0 0;
	margin: 0 0 0.3em 0;
}

a {
	cursor: pointer; 
	text-decoration: none;
	color: black;
}

.icon {
	height: 1em;
	margin: 0 0.4rem 0 0; 
}

.descriptionHTML {
	margin: 1em 0;
	padding: 1em; 
	border: 1px solid black; 
}

.show {
}

</style>
