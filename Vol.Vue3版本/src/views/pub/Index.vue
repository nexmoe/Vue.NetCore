<template>
	<el-container>
		<Header />
		<el-main class="nexmoe-main">
			<el-input
				v-model="keywords"
				placeholder="在这里搜索"
				class="nexmoe-search"
			>
				<template #append>
					<el-button icon="el-icon-search" />
				</template>
			</el-input>
			<section>
				<header>
					<h2>
						<i class="el-icon-star-on"></i>
						<span>热门</span>
					</h2>
				</header>
				<el-row :gutter="24">
					<el-col v-for="(o, index) in 8" :key="o" :span="6">
						<Card />
					</el-col>
				</el-row>
			</section>
			<section class="xueyuan">
				<header>
					<h2>
						学院导航
					</h2>
				</header>
				<el-row :gutter="24">
					<el-col v-for="(o, index) in 20" :key="o" :span="6">
						<span>宇宙机学院（233）</span>
					</el-col>
				</el-row>
			</section>
		</el-main>
		<el-footer><Footer /></el-footer>
	</el-container>
</template>

<script setup>
import "nexmoe.css";
import Card from "./components/Card.vue";
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
import { ref } from "vue";
const keywords = ref("");
const currentDate = ref(new Date());
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
.xueyuan {
	color: #fff;
	padding: 2rem;
	background-color: #0e559f;
	box-shadow: 3px 3px 0px 3px #002954 !important;
}
</style>
