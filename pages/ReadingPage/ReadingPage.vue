<template>
	<view>
		{{content}}
	</view>
</template>

<script>
	export default {
		data() {
			return {
				content: "What you lookin' at? You all a bunch of fuckin' assholes. You know why? You don't have the guts to be what you wanna be? You need people like me. You need people like me so you can point your fuckin' fingers and say, \"That's the bad guy.\" So... what that make you? Good? You're not good. You just know how to hide, how to lie. Me, I don't have that problem. Me, I always tell the truth. Even when I lie. So say good night to the bad guy! Come on. The last time you gonna see a bad guy like this again, let me tell you. Come on. Make way for the bad guy. There's a bad guy comin' through! Better get outta his way!"
			}
		},
		onLoad: function(option) { //option为object类型，会序列化上个页面传递的参数
			console.log(option.id); //打印出上个页面传递的参数。
			uni.setNavigationBarTitle({
				title: option.Title
			});
		}
	}
</script>

<style>

</style>
