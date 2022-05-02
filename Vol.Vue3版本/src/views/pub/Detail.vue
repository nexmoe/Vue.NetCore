<template>
	<el-card class="nexmoe-card" :body-style="{ padding: '0px' }">
		<div class="common-layout">
			<el-container>
				<el-aside class="nexmoe-aside" width="260px">
					<div class="text nexmoe-info">
						<img
							src="https://pic1.zhimg.com/50/v2-6afa72220d29f045c15217aa6b275808_hd.jpg?source=1940ef5c"
							class="nexmoe-image"
						/>
						<ul>
							<template v-for="info in infoList">
								<li v-if="item[info.key]">
									<span>{{ info.title }}：</span>
									{{ item[info.key] }}
								</li>
							</template>
						</ul>
					</div>
				</el-aside>
				<el-main>
					<el-tabs
						v-model="activeName"
						class="demo-tabs"
						@tab-click="handleClick"
					>
						<el-tab-pane
							v-for="tab in tabList"
							:label="tab.title"
							:name="tab.key"
						>
							<div class="text" v-html="item[tab.key]"></div>
						</el-tab-pane>
					</el-tabs>
				</el-main>
			</el-container>
		</div>
	</el-card>
</template>

<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";

const infoList = [
	{ key: "dsxm", title: "姓名" },
	{ key: "xb", title: "性别" },
	{ key: "xsmc", title: "学院" },
	{ key: "yddh", title: "手机号" },
	{ key: "dwdh", title: "单位电话" },
	{ key: "zzdh", title: "住宅电话" },
	{ key: "GBZW", title: "行政职务" },
	{ key: "csrq", title: "出生日期" },
	{ key: "zcmc", title: "职称" },
	{ key: "mz", title: "民族" },
	{ key: "zzmm", title: "政治面貌" },
	{ key: "status", title: "状态" },
	{ key: "role", title: "角色" },
	{ key: "pzsdny", title: "聘任硕导年月" },
	{ key: "pzbdny", title: "聘任博导年月" },
	{ key: "dslb", title: "导师类别" },
	{ key: "yjxkdm", title: "一级学科代码" },
	{ key: "yjxk", title: "一级学科" },
	{ key: "zylydm", title: "专业领域代码" },
	{ key: "zyly", title: "专业领域" },
	{ key: "cszymc1", title: "从事专业1" },
	{ key: "cszymc2", title: "从事专业2" },
	{ key: "cszymc3", title: "从事专业3" },
];

const tabList = [
	{ key: "dsjl", title: "导师简历" },
	{ key: "bz", title: "备注" },
	{ key: "jbqk", title: "基本情况" },
	{ key: "yjfxqk", title: "研究方向介绍" },
	{ key: "kyqk", title: "科研情况" },
	{ key: "hjqk", title: "获奖情况" },
	{ key: "qtqk", title: "其他情况" },
];

const router = useRouter().currentRoute.value;
const item = ref({});
const activeName = ref("jbqk");

fetch("http://10.30.0.151:8081/api/dsxx/" + router.params.id)
	.then((response) => response.json())
	.then((res) => {
		console.log(res);
		item.value = res;
	});
</script>

<style scoped>
.nexmoe-card {
	margin-top: 24px;
	border-radius: 0;
	border: none;
}
.nexmoe-aside {
	padding: 24px;
	background-color: rgb(240, 240, 240);
}
.nexmoe-image {
	width: 100%;
	height: 100%;
	border-radius: 0;
	border: 2px solid;
}
.nexmoe-info {
	color: #777777;
}
.nexmoe-info ul {
	list-style: none;
	padding: 0;
}
.nexmoe-info span {
	font-weight: bold;
	color: #333333;
}
section,
main {
	margin: 0;
}
</style>
