<script setup lang="ts">
	import { ref } from 'vue'
	defineProps({
		message: {
			type: String,
		},
	})
	const count = ref(0)
</script>

<template>
	<v-sheet
		min-height="70vh"
		rounded="lg"
		class="pa-6 text-center"
	>
		<h1>{{ $route.query.message }}</h1>
		<h4>{{ message }}</h4>
		<div class="card">
			<button
				type="button"
				@click="count++"
			>
				count is {{ count }}
			</button>
			<p>
				Edit
				<code>components/HelloWorld.vue</code> to test HMR
			</p>
		</div>

		<p>
			Check out
			<a
				href="https://vuejs.org/guide/quick-start.html#local"
				target="_blank"
				>create-vue</a
			>, the official Vue + Vite starter
		</p>
		<p>
			Learn more about IDE Support for Vue in the
			<a
				href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
				target="_blank"
				>Vue Docs Scaling up Guide</a
			>.
		</p>
		<p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
	</v-sheet>
</template>

<style scoped>
	.read-the-docs {
		color: #888;
	}
</style>
