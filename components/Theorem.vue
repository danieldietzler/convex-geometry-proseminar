<script setup>
	defineProps(['label'])
</script>

<template>
	<div class="p-4 shadow-lg">
		<h3 class="underline">Theorem {{ label }}</h3>
		<slot/>
	</div>
</template>