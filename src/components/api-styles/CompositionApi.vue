<script setup lang="ts">
import { onMounted, ref } from 'vue'

defineProps<{ title: string }>()

// reactive state
const count = ref(0)

// functions that mutate state and trigger updates
function increment() {
	count.value++
}

// lifecycle hooks
onMounted(() => {
	console.log(`The initial count is ${count.value}.`)
})
</script>

<template>
	<div>
		<h1 class="title">{{ title }}</h1>
		<button class="button" @click="increment">Count is: {{ count }}</button>
	</div>
</template>

<style scoped>
.title {
	font-size: 4rem;
	color: #646cff;
}

.button {
	background-color: chartreuse;
	color: white;
	border: none;
	padding: 10px 20px;
	font-size: 16px;
	cursor: pointer;
	border-radius: 5px;
	transition: background-color 0.3s ease;
}
</style>
