<template>
	<el-input v-model="keywords" placeholder="在这里搜索" class="nexmoe-search">
		<template #append>
			<el-button icon="el-icon-search" />
		</template>
	</el-input>
	<section>
		<header>
			<h2>
				<span>{{ keywords ? `“${keywords}”的搜索结果` : "热门" }}</span>
			</h2>
		</header>
		<el-row :gutter="24">
			<el-col v-for="(item, index) in dataList" :key="index" :span="6">
				<router-link :to="'/pub/detail/' + item.dsbh">
					<Card :item="item" />
				</router-link>
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
	<el-pagination
		background
		v-model:currentPage="pageNow"
		:page-size="16"
		layout="prev, pager, next"
		:total="dataTotal"
	/>
</template>

<script setup>
import Card from "./components/Card.vue";
import { useRouter } from "vue-router";
import { ref, watch } from "vue";
const keywords = ref("");
const dataList = ref([]);
const pageNow = ref(1);
const dataTotal = ref(0);

const getDataBykeyword = () => {
	fetch(
		"http://10.30.0.151:8081/api/dsxx/SearchPage?pageIndex=" +
			pageNow.value +
			"&pagesize=12" +
			"&search=" +
			keywords.value
	)
		.then((response) => response.json())
		.then((res) => {
			console.log(res);
			dataList.value = res.data;
			dataTotal.value = res.count;
		});
};

const getData = () => {
	fetch(
		"http://10.30.0.151:8081/api/dsxx/CommonPage?pageIndex=" +
			pageNow.value +
			"&pagesize=12"
	)
		.then((response) => response.json())
		.then((res) => {
			console.log(res);
			dataList.value = res.data;
			dataTotal.value = res.count;
		});
};

getData();

watch(keywords, () => {
	if (keywords.value) {
		getDataBykeyword();
	}
});

watch(pageNow, () => {
	keywords.value ? getDataBykeyword() : getData();
});
console.log("Made By Nexmoe");
</script>

<style scoped>
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
