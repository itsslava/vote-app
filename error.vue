<script setup lang="ts">
import type { NuxtError } from '#app';

const { error } = defineProps<{ error: NuxtError }>();
</script>
<template>
	<div class="error-wrapper">
		<h1 class="error-code">{{ error.statusCode }}</h1>
		<div v-if="error.statusCode == 404" class="error-message">
			Страница не найдена, вернитесь на главную страницу
		</div>
		<div v-else class="error-message">{{ error.statusMessage }}</div>
		<TextButton size="l">На главную</TextButton>
	</div>
</template>
<style scoped>
.error-wrapper {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

.error-code {
	font-weight: 500;
	font-size: 120px;
	color: var(--color-black-light);
}
.error-message {
	color: var(--color-black-light);

	font-size: 16px;
	text-align: center;

	padding-bottom: 24px;

	font-weight: 100;

	letter-spacing: 0%;
}
</style>
