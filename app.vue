<script setup lang="ts">
import '@fontsource/fira-mono';
import '@fontsource/inter';
import '@fontsource/poppins';
import { THEMES, useThemeStore } from './store/theme';

const themeStore = useThemeStore();
</script>

<template>
	<div
		:data-theme="themeStore.theme.dark ? THEMES.DARK : THEMES.LIGHT"
		class="bg-gradient-to-r from-base-100 to-neutral"
	>
		<div class="max-w-8xl mx-auto pt-4 pr-8 pb-8 pl-8">
			<Header />
			<NuxtPage />
			<NuxtLayout name="custom" />
		</div>
	</div>
</template>
