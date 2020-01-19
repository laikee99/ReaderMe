<template name="BookCard">
	<view class="CardContent" @tap="ToRead">
		<view class="BookName">{{BookName}}</view>
		<DivLine></DivLine>
		<view class="BookContent">
			<image class="BookPic" mode="aspectFit" :src="BookPic"></image>
			<view>{{BookContent}}</view>
		</view>
	</view>
</template>

<script>
	//引入分割线组件
	import DivLine from "./DivLine.vue"
	export default {
		name: "BookCard",
		props: {
			BookName: {
				type: String,
				default: "书名"
			},
			BookContent: {
				type: String,
				default: "在这里我们存放一段关于本书的简介。"
			},
			BookPic: {
				type: String,
				default: "../../static/DefaultPicture/BookPic_Default.png"
			}
		},
		components: {
			DivLine
		},
		methods: {
			ToRead() {
				uni.navigateTo({
					url: '../ReadingPage/ReadingPage?Title=弟弟行为'
				})
			}
		}
	}
</script>

<style scoped>
	.CardContent {
		/*背景颜色*/
		background: #9CCDD9;
		/*圆角设置*/
		border-radius: 15upx;
		/*边框宽度*/
		/*padding: 5upx;*/
		/*宽度设置*/
		width: 95%;
		/*背景颜色*/
		display: flex;
		flex-direction: column;
		/*边缘距离*/
		margin: 15upx;
	}

	.BookName,
	.BookContent,
	.BookPic {
		/*离边缘距离*/
		margin: 5upx 5upx 5upx 5upx;
	}

	.BookName {
		/*书名字体大小*/
		font-size: 14px;
	}

	.BookContent {
		/*书内容简介布局*/
		display: flex;
		/*横向*/
		flex-direction: row;
		/*垂直居中*/
		align-items: center;
		/*字体大小*/
		font-size: 10px;
	}

	.BookPic {
		/*书籍图片*/
		/*宽度设置*/
		min-width: 15%;
		max-width: 20%;
		/*长度设置*/
		min-height: 50upx;
		max-height: 150upx;
		/*圆角设置*/
		border-radius: 5px;
	}
</style>
