<template>
	<view class="content">
		<view class="BookShelf">
			<BookCard v-for="i in 5" :key="i" :BookName="BookName"></BookCard>
		</view>
	</view>
</template>

<script>
	import BookCard from "../../components/BookCard.vue"
	export default {
		components: {
			BookCard
		},
		data() {
			return {
				BookName: "这是一段测试书名"
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped>
	.content,
	.BookShelf {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
</style>
