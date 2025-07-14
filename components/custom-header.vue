<template>
	<header class="custom-header">
		<NuxtLink to="/"><Icon name="icons:home" size="24px" /></NuxtLink>
		<div class="header-bottom">
			<NuxtLink to="/"><Icon name="icons:profile" size="24px" /></NuxtLink>
			<NuxtLink to="/"><Icon name="icons:logout" size="24px" /></NuxtLink>
		</div>
	</header>
</template>
<style lang="css" scoped>
.custom-header {
	display: flex;
	flex-direction: column;
	justify-content: space-between;

	padding: 42px 28px;
	margin-right: 130px;

	border-right: 1px solid var(--color-light-gray);
}
.header-bottom {
	display: flex;
	flex-direction: column;
	gap: 20px;
}

.custom-header a {
	text-decoration: none;
	color: var(--color-black);
	transition: color 0.3s ease;
}

.custom-header a:hover {
	color: var(--color-dark-gray);
}
</style>
