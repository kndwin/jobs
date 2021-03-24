<template>
  <div class="container">
		<Header class="header"/>
    <nuxt class="main" />
		<Footer class="footer"/>
  </div>
</template>

<style lang="scss">

	body {
		font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif; 
	}
	.container {
		min-height: 100%;
	}

	.header {
	}

	.main {
		flex: 1; 
	}

	.footer {
	}
</style>
