<template>
	<el-container>
		<Header />
		<el-main class="nexmoe-main">
			<DetailCard />
		</el-main>
		<el-footer><Footer /></el-footer>
	</el-container>
</template>

<script setup>
import "nexmoe.css";
import DetailCard from "./components/DetailCard.vue";
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
import { ref } from "vue";
console.log("Made By Nexmoe");
</script>

<style>
:root {
	--color-primary: #0e559f;
	--color-hover: rgba(14, 85, 159, 0.15);
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
	width: 960px;
	margin: 0 auto;
}
.nexmoe-search {
	margin-top: 48px;
	zoom: 1.5;
}
</style>
