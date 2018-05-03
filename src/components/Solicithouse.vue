<template>
	<section class="content-wrap">	
		<div class="matters">
			<a href="http://woke.jiugubao.com/">
				<h1>蜗客商城(PC)</h1>
				<p>网上购物商城。</p>
				<p>页面采用了DIV+CSS的布局方式，JavaScript实现页面的一些动态效果;</p>
				<p>使用Bootstrap框架对页面进行布局，使页面具有响应式布局，达到良好的用户体验</p>
			</a>
		</div>
		<div class="matters">
			<a href="http://woke.jiugubao.com/">
				<h1>蜗客商城(WEB)</h1>
				<p>采用阿里的UI组件库sui，采用了面向对象的方法，将常用的方法封装在一个js内;</p>
				<p>使用 ajax和后端通讯，关于支付模块，调用ping++所提供接口及文档完成支付。</p>
			</a>
		</div>
		<div class="matters">
			<a href="http://app.iwoke.club/">
				<h1>蜗客校园</h1>
				<p>用vue构建的单页应用，vue-router前端路由进行页面跳转;</p>
				<p>使用MintUI组件库，前端页面快速构建;</p>
				<p>使用axios和后端进行数据交互，利用less来编写项目的样式，使项目样式更加方便管理。</p>
			</a>
		</div>
		<div class="matters">
			<a href="http://xiu.iwoke.club/">
				<h1>咻咻咻</h1>
				<p>用vue构建的单页应用，使用MintUI组件库;</p>
				<p>利用less编写项目样式，引用了photoswipe插件对显示图片进行处理，可供用户查看大图;</p>
				<p>使用iscroll插件对页面进行分页数据显示，使用vue-star组件来实现用户点赞特效，增加用户体验。</p>
			</a>
		</div>
	</section>

</template>

<style scoped>
section.content-wrap {
  position: relative;
}
.matters {
  padding-left: 300px;
  margin-top: 50px;
}
.matters h1 {
  font-size: 24px;
  line-height: 100px;
  margin-left: 75px;
}
.matters p {
  line-height: 40px;
  margin-left: 83px;
}
</style>
<script>
export default {};
</script>
