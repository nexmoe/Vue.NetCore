<template>
	<el-card
		class="nexmoe-card"
		:body-style="{ padding: '0px' }"
	>
		<img
			src="https://pic1.zhimg.com/50/v2-6afa72220d29f045c15217aa6b275808_hd.jpg?source=1940ef5c"
			class="nexmoe-image"
		/>
		<div class="nexmoe-major">
			<span>{{ props.item.dsxm }}</span><br>
			<span>{{ props.item.xsmc }}</span>
		</div>
	</el-card>
</template>

<script setup>
const props = defineProps(['item'])
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
	height: 100%;
	border-radius: 0;
	border: none;
}
.nexmoe-major {
	padding: 1rem;
	font-size: 1.2rem;
	font-weight: bold;
}
</style>
