<template>
  <div class="container">
		<Header class="header"/>
    <nuxt class="main" />
		<Footer class="footer"/>
  </div>
</template>

<style lang="scss">

html, body {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',Roboto, 'Helvetica Neue', Arial, sans-serif; 
  height: 100%;
}
body {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.container {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  max-width: 800px;
  width: 100%;
}

.header {
}

.main {
}

.footer {
}
</style>
