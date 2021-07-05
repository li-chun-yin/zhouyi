<template>
	<view class="wrap">
		<u-grid :col="4" class="gua-lists" v-for="group in items.groups" :key="group">
			<view class="u-font-36">{{ group.title }}</view>
			<u-line />
			<u-grid-item v-for="item in group.lists " :key="item">
				<view class="shape">{{ item.shape }}</view>
				<view class="name">{{ item.name }}</view>
			</u-grid-item>
		</u-grid>
	</view>
</template>

<script>
export default {
	data() {
		return {
			items: {groups: [{
				title: '上经三十卦',
				lists: [{
							shape: '䷀',
							name: '乾'
						},{
							shape: '䷁',
							name: '坤'
						},{
							shape: '䷁',
							name: '屯'
						},{
							shape: '䷃',
							name: '蒙'
						},{
							shape: '䷄',
							name: '需'
						},{
							shape: '䷅',
							name: '讼'
						},{
							shape: '䷆',
							name: '师'
						},{
							shape: '䷇',
							name: '比'
						},{
							shape: '䷈',
							name: '小畜'
						},{
							shape: '䷉',
							name: '履'
						},{
							shape: '䷊',
							name: '泰'
						},{
							shape: '䷋',
							name: '否'
						},{
							shape: '䷌',
							name: '同人'
						},{
							shape: '䷍',
							name: '大有'
						},{
							shape: '䷎',
							name: '谦'
						},{
							shape: '䷏',
							name: '豫'
						},{
							shape: '䷐',
							name: '随'
						},{
							shape: '䷑',
							name: '蛊'
						},{
							shape: '䷒',
							name: '临'
						},{
							shape: '䷓',
							name: '观'
						},{
							shape: '䷔',
							name: '噬嗑'
						},{
							shape: '䷕',
							name: '贲'
						},{
							shape: '䷖',
							name: '剥'
						},{
							shape: '䷗',
							name: '复'
						},{
							shape: '䷘',
							name: '无妄'
						},{
							shape: '䷙',
							name: '大畜'
						},{
							shape: '䷚',
							name: '颐'
						},{
							shape: '䷛',
							name: '大过'
						},{
							shape: '䷜',
							name: '坎'
						},{
							shape: '䷝',
							name: '离'
					}]
				},{
				'title': '下经三十四卦',
				'lists': [{
					shape: '䷞',
					name: '咸'
				},{
					shape: '䷟',
					name: '恒'
				},{
					shape: '䷠',
					name: '遁'
				},{
					shape: '䷡',
					name: '大壮',
				},{
					shape: '䷢',
					name: '晋',
				},{
					shape: '䷣',
					name: '明夷',
				},{
					shape: '䷤',
					name: '家人',
				},{
					shape: '䷥',
					name: '睽',
				},{
					shape: '䷦',
					name: '蹇',
				},{
					shape: '䷧',
					name: '解',
				},{
					shape: '䷨',
					name: '损',
				},{
					shape: '䷩',
					name: '益',
				},{
					shape: '䷪',
					name: '夬',
				},{
					shape: '䷫',
					name: '姤',
				},{
					shape: '䷬',
					name: '萃',
				},{
					shape: '䷭',
					name: '升',
				},{
					shape: '䷮',
					name: '困',
				},{
					shape: '䷯',
					name: '井',
				},{
					shape: '䷰',
					name: '革',
				},{
					shape: '䷱',
					name: '鼎',
				},{
					shape: '䷲',
					name: '震',
				},{
					shape: '䷳',
					name: '艮',
				},{
					shape: '䷴',
					name: '渐',
				},{
					shape: '䷵',
					name: '归妹',
				},{
					shape: '䷶',
					name: '丰',
				},{
					shape: '䷷',
					name: '旅',
				},{
					shape: '䷸',
					name: '巽',
				},{
					shape: '䷹',
					name: '兑',
				},{
					shape: '䷺',
					name: '涣',
				},{
					shape: '䷻',
					name: '节',
				},{
					shape: '䷼',
					name: '中孚',
				},{
					shape: '䷽',
					name: '小过',
				},{
					shape: '䷾',
					name: '既济',
				},{
					shape: '䷿',
					name: '未济',
				}]
			}]},
			search:{
				page: 1,
				limit: 10
			},
			hast_next_page: false
		}
	},
	onLoad(e) {
	},
	onReachBottom(e){
	},
	methods:{
		loadData(){
		}
	}
};
</script>

<style scoped lang="scss">
	.gua-lists .shape {
		font-size: 96rpx;
	}
	.gua-lists .name {
		font-size: 64rpx;
	}
</style>
