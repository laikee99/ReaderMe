<template name="BookCard">
	<view class="CardContent">
		<view class="BookName">{{BookName}}</view>
		<DivLine></DivLine>
		<view class="BookContent">
			<image class="BookPic" mode="aspectFit" :src="BookPic"></image>
			<view>{{BookContent}}</view>
		</view>
	</view>
</template>

<script>
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
				default: "这里是属于斗气的世界，没有花俏艳丽的魔法，有的，仅仅是繁衍到巅峰的斗气！新书等级制度：斗者，斗师，大斗师，斗灵，斗王，斗皇，斗宗，斗尊，斗圣，斗帝。"
			},
			BookPic: {
				type: String,
				default: "/static/logo.png"
			}
		},
		components: {
			DivLine
		}
	}
</script>

<style scoped>
	.CardContent {
		/*背景颜色*/
		background: #007AFF;
		/*圆角设置*/
		border-radius: 15upx;
		/*边框宽度*/
		/*padding: 5upx;*/
		/*宽度设置*/
		width: 95%;
		/*背景颜色*/
		display: flex;
		flex-direction: column;
	}

	.BookName,
	.BookContent,
	.BookPic {
		margin: 5upx 5upx 5upx 5upx;
	}

	.BookContent {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.BookPic {
		min-width: 33%;
		max-width: 40%;
		max-height: 250upx;
	}
</style>
