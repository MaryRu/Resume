<template>
	<div id="sidebar">
		<ul>
			<li v-for="(item,index) in sidebarList" class="list-item">
				<router-link :to="item.url">{{item.content}}</router-link>
			</li>
		</ul>
	</div>
</template>

<script>

export default {
	
	data() {
		return {
			sidebarList: [],
			customerSidebar: [
				{content: '个人信息', url: '/matters'},
				{content: '教育背景', url: '/renthouse'},
				{content: '个人经历', url: '/sellhouse'},
				{content: '项目经验', url: '/solicithouse'},
				{content: '个人技能', url: '/modifypass'},
				{content: '联系我', url: '/userinfo'}
			]
		}
	},

	created() {
		if (sessionStorage.userid) {
			this.sidebarList = this.sidebarList.concat(this.adminSidebar)
		} else {
			this.sidebarList = this.sidebarList.concat(this.customerSidebar)
		}
	},
	
	methods: {
		
	}
}
</script>

<style scoped>
#sidebar{
	position: fixed;
	padding-top: 30px;
	width: 180px;
	height: 100%;
	z-index: 10;
	border-right: 1px solid #fff;
}
.list-item{
	height: 50px;
	line-height: 50px;
	text-align: center;
	font-family: '微软雅黑';
}
.list-item a.active{
	display: block;
	background: rgba(7,17,27,1);
}
</style>