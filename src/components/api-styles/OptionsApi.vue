<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
	props: {
		title: String,
	},
	name: "OptionsApi",

	// Properties returned from data() become reactive state
	// and will be exposed on `this`.
	data() {
		return {
			count: 0
		}
	},

	// Methods are functions that mutate state and trigger updates.
	// They can be bound as event handlers in templates.
	methods: {
		increment() {
			this.count++
		}
	},

	// Lifecycle hooks are called at different stages
	// of a component's lifecycle.
	// This function will be called when the component is mounted.
	mounted() {
		console.log(`The initial count is ${this.count}.`)
	}
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
	color: blueviolet;
}

.button {
	background-color: #42b883;
	color: white;
	border: none;
	padding: 10px 20px;
	font-size: 16px;
	cursor: pointer;
	border-radius: 5px;
	transition: background-color 0.3s ease;
}
</style>
