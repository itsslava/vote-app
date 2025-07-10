<script setup lang="ts">
const { size = 'l' } = defineProps<{ size?: 'l' | 's' }>();
</script>
<template>
	<button :class="['btn', size === 'l' ? 'btn-l' : 'btn-s']"><slot /></button>
</template>
<style scoped>
.btn {
	background-color: var(--color-black);
	border: none;
	border-radius: 20px;

	font-weight: 500;
	font-size: 16px;
	text-align: center;
	color: var(--color-white);

	cursor: pointer;

	padding: 12px;

	transition: all 0.2s ease-in-out;
}
.btn:hover {
	background-color: var(--color-black-hover);
}
.btn-l {
	min-width: 301px;
}
.btn-s {
	min-width: 141px;
}
</style>
