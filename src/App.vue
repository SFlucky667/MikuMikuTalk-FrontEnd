<script setup lang="ts">
import { useUserStore } from '@/stores';

const store = useUserStore();
store.loadUserInfo();
store.loadUserProfile();
</script>

<template>
	<div class="main">
		<div class="background-blur"></div>

		<RouterView />
	</div>
</template>

<style scoped lang="scss">
.main {
	width: 100%;
	height: 100vh;
	/* 确保父元素有明确的高度 */
	display: flex;
	flex-direction: column;
	align-items: center;
	/* 垂直居中 */
	justify-content: center;
	/* 水平居中 */
}

.background-blur {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background-image: url('https://blog.meowrain.cn/api/i/2024/12/11/emeoFj1733886699479520138.webp');
	background-repeat: no-repeat;
	background-position: center;
	background-size: cover;
	filter: blur(8px);
	/* 添加模糊效果 */
	z-index: -1;
	/* 确保模糊层在内容后面 */
}
</style>
