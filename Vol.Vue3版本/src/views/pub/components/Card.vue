<template>
	<el-card class="nexmoe-card" :body-style="{ padding: '0px' }">
		<img :src="getUserImg(item.HeadImageUrl)" class="nexmoe-image" />
		<div class="nexmoe-major">
			<span>{{ props.item.dsxm }}</span><br>
			<span>{{ props.item.xsmc || "　" }}</span>
		</div>
	</el-card>
</template>

<script setup>
import { getCurrentInstance } from "vue";
import http from "@/../src/api/http.js";
const props = defineProps(['item'])
let _config = getCurrentInstance().appContext.config.globalProperties;
const getUserImg = (HeadImageUrl) => {
	if (HeadImageUrl) {
		return _config.base.getImgSrc(HeadImageUrl, http.ipAddress);
	} else {
		return require('@/assets/imgs/avatar.png')
	}
}
</script>

<style scoped>
.nexmoe-card {
	margin-top: 24px;
	background-color: #0e559f;
	box-shadow: 3px 3px 0px 3px #002954 !important;
	border-radius: 0;
	border: none;
	color: #fff;
}

.nexmoe-image {
	width: 100%;
	height: 212px;
	border-radius: 0;
	border: none;
}

.nexmoe-major {
	padding: 1rem;
	font-size: 1.2rem;
	font-weight: bold;
}
</style>
