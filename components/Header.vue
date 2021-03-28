<template>
	<div class="header">
		<NuxtLink to="/" class="link">
			<img class="logo" src="~/assets/Icon.webp" 
				alt="Logo"
			>
    </NuxtLink>
		<NuxtLink to="/jobs" class="link">
      jobs
    </NuxtLink>
	</div>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  align-items: center;
  padding: 1rem;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 7rem;

  a {
    text-decoration: none;
    font-size: 14pt;
    color: black;
    font-weight: bold;
  }
}

.link {
  margin: 0 1rem;
}

.logo {
	height: 3rem;
}
</style>
