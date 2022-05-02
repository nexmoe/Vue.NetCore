<template>
	<el-container>
		<Header />
		<el-main class="nexmoe-main">
			<router-view></router-view>
		</el-main>
		<el-footer><Footer /></el-footer>
	</el-container>
</template>

<script setup>
import "nexmoe.css";
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
console.log("Made By Nexmoe");
</script>

<style>
:root {
	--color-primary: #0e559f;
	--color-hover: rgba(14, 85, 159, 0.15);
    --hover-brightness: 1.15;
}
body {
	background-color: #eff7fd;
	overflow-x: hidden;
}
</style>

<style scoped>
.el-container {
	margin: 0;
}
.el-footer {
	padding: 0;
	margin: 0;
}
.nexmoe-main {
	margin: 0 auto;
}
</style>
