<template>
	<div id="header">
		<div class="logo">
			关于<span style="font-size: 20px;font-weight:normal">马玉茹</span>
		</div>
		<div class="user" @mouseover="showUserX()">
			<img class="avatar" src="../assets/images/avatar.png" alt="">
			Mary Ru
		</div>
	</div>
</template>

<script>

export default {
	data() {
		return {
			isAdmin: false,
			show: false,
			name: 'MaryRu'
		}
	},
	created() {
		this.name = sessionStorage.name
		if (sessionStorage.userid) {
			this.isAdmin = true
		}
	},
	methods: {
		showUserX() {
			this.show = true
		},
		hideUserX() {
			this.show = false
		},
		logOut() {
			if (sessionStorage.userid) {
				sessionStorage.id = ''
				sessionStorage.userid = ''
				sessionStorage.name = ''		
			} else {
				sessionStorage.id = ''
				sessionStorage.name = ''	
			}

			this.$router.push('/menu')
		}
	}
}
</script>

<style scoped>
#header{
	position: relative;
	height: 80px;
	line-height: 80px;
	display: flex;
	padding: 0 20px;
	justify-content: space-between;
	z-index: 12;
}
.logo{
	font-size: 26px;
	font-weight: 600;
}
.logo span{
	font-size: 16px;
	margin-left: 15px;
}
.user{
	font-size: 16px;
}
.user .avatar{
	width: 50px;
	height: 50px;
	border-radius: 50%;
	vertical-align: middle;
	margin-right: 10px;
}
.user .icon{
	width: 17px;
    height: 17px;
    margin-left: 5px;
    vertical-align: middle;
}
.user-x{
	position: absolute;
	right: 20px;
	top: 70px;
	width: 100px;
	height: 100px;
	z-index: 1000;
}
.user-x ul li{
	list-style: none;
	width: 100px;
	height: 50px;
	line-height: 50px;
	text-align: center;
	cursor: pointer;
}
.user-x ul li a{
	display: block;
}
.user-x ul li:hover{
	background: rgba(7,17,27,.5);
}
</style>