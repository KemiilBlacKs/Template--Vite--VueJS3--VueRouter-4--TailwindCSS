<script setup>
	// This starter template is using Vue 3 <script setup> SFCs
	// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
	import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
	<router-view v-slot="{ Component, route }">
		<transition appear name="fade">
			<div :key="route.name">
				<component :is="Component" />
			</div>
		</transition>
	</router-view>
</template>

<style>
	.fade-enter-active,
	.fade-leave-active {
		transition: opacity 0.3s ease-in-out;
	}

	.fade-enter-from,
	.fade-leave-to {
		opacity: 0;
	}
</style>
