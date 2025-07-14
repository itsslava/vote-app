<template>
	<div class="default-layout">
		<CustomHeader />
		<main><slot /></main>
	</div>
</template>
<style lang="css" scoped>
.default-layout {
	display: flex;
	height: 100vh;
}
</style>
