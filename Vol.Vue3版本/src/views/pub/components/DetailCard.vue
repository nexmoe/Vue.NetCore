<template>
	<el-card class="nexmoe-card" :body-style="{ padding: '0px' }">
		<div class="common-layout">
			<el-container>
				<el-header
					><el-menu
						:default-active="activeIndex"
						class="el-menu-demo"
						mode="horizontal"
						@select="handleSelect"
					>
						<el-menu-item index="1">Processing Center</el-menu-item>
						<el-menu-item index="3">Info</el-menu-item>
						<el-menu-item index="4">Orders</el-menu-item>
					</el-menu></el-header
				>
				<el-container>
					<el-aside class="nexmoe-aside" width="240px">
						<header>
							<h3>个人信息</h3>
						</header>
						<div class="text">
							副教授 硕士生导师<br />性别：男<br />毕业院校：大连理工大学
							学位：博士<br />所在单位：控制科学与工程学院<br />
							学科：控制理论与控制工程<br />办公地点：创新园大厦
							A732<br />
							电子邮箱：qiu@dlut.edu.cn
						</div>
					</el-aside>
					<el-main>
						<h1>个人简介</h1>
						<div class="text">
							感恩母校大工，University of Essex
							计算机系联合培养博士，生物医学工程博士后；现为电信学部部长助理，入选大连理工大学星海骨干，大连市高层次人才，教育部科技发展中心优秀借调干部。
							编写教材一部，主持教育部产学研协同育人教改项目，获全国教师教育教学信息化交流活动一等奖，校教学质量优良奖，讲课竞赛校二等奖、学部一等奖；校优秀专业班主任，优秀共产党员。
							研究兴趣为可穿戴与医工交叉，3次获得国际会议最佳论文奖，获中国石油化学工业联合会科技进步二等奖，辽宁省自然科学学术成果一等奖；谷歌学术引用超过1250次,
							H指数20，ESI高被引论文1篇；获国家发明专利5项、国际专利1项，主持国家自然科学青年基金、中国博士后面上基金、辽宁省和大连市科技创新基金、以及中央高校交叉探索专题等多项科研项目，参与多项国家级项目，致力于智能可穿戴计算、多源异构信息融合、无线传感器网络领域的研究。
							坚持总书记提出的“四个面向”要求，针对穿戴式多生命体征智能监测、物联网技术应用与人工智能等关键问题开展理论与技术研究，努力实现传感器、多模态信息、人机交互、健康监测技术的深度融合，在特殊应用场景下的个体化穿戴式健康监测与智能交互领域形成原创性理论成果和实用设备。
						</div>
					</el-main>
				</el-container>
			</el-container>
		</div>
	</el-card>
</template>

<script setup>
import { ref } from "vue";

const activeIndex = ref("1");
const handleSelect = (key, keyPath) => {
	console.log(key, keyPath);
};
</script>

<style>
.nexmoe-card {
	margin-top: 24px;
	box-shadow: 3px 3px 0px 3px #002954 !important;
	border-radius: 0;
	border: none;
}
.nexmoe-aside {
	padding: 24px;
}

section,
main {
	margin: 0;
}
</style>
