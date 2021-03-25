<template>
	<div>
		<h1>Jobs dashboard</h1>		
		<Job v-for="job in jobs" :key="job.link" :id="job.title" :job="job" />
	</div>
</template>


<script lang="ts">
	import Vue from 'vue'
	import axios from 'axios'
	export default Vue.extend({
		
		async created() {
			try {
				const res = await axios.get("https://jobscraps.herokuapp.com/jobs")
				this.jobs = await res.data
			} catch (err) {
				console.log(err)
			}
		},
		fetchOnServer: true,
    data() {
      return {
        jobs: []
      }
    },
	})
</script>
