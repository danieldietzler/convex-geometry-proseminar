<script setup>
	defineProps(['label'])
</script>

<template>
	<div class="p-4 shadow-lg">
		<h3 class="underline">Definition {{ label }}</h3>
		<slot/>
	</div>
</template>