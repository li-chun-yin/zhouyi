<template>
	<view class="wrap">
		<u-grid :col="4" class="gua-lists" v-for="group, index in items.groups" :key="index">
			<view class="title">{{ group.title }}</view>
			<u-line />
			<u-grid-item v-for="item, key in group.lists " :key="key">
				<navigator :url="'/pages/gua-desc?code='+item.code">
					<view class="shape">{{ item.shape }}</view>
					<view class="name">{{ item.name }}</view>
				</navigator>
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
							name: '乾',
							code: '111111'
						},{
							shape: '䷁',
							name: '坤',
							code: '000000'
						},{
							shape: '䷂',
							name: '屯',
							code: '010001'
						},{
							shape: '䷃',
							name: '蒙',
							code: '100010'
						},{
							shape: '䷄',
							name: '需',
							code: '010111'
						},{
							shape: '䷅',
							name: '讼',
							code: '111010'
						},{
							shape: '䷆',
							name: '师',
							code: '000010'
						},{
							shape: '䷇',
							name: '比',
							code: '010000'
						},{
							shape: '䷈',
							name: '小畜',
							code: '110111'
						},{
							shape: '䷉',
							name: '履',
							code: '111011'
						},{
							shape: '䷊',
							name: '泰',
							code: '000111'
						},{
							shape: '䷋',
							name: '否',
							code: '111000'
						},{
							shape: '䷌',
							name: '同人',
							code: '111101'
						},{
							shape: '䷍',
							name: '大有',
							code: '101111'
						},{
							shape: '䷎',
							name: '谦',
							code: '000100'
						},{
							shape: '䷏',
							name: '豫',
							code: '001000'
						},{
							shape: '䷐',
							name: '随',
							code: '011001'
						},{
							shape: '䷑',
							name: '蛊',
							code: '100110'
						},{
							shape: '䷒',
							name: '临',
							code: '000011'
						},{
							shape: '䷓',
							name: '观',
							code: '110000'
						},{
							shape: '䷔',
							name: '噬嗑',
							code: '101001'
						},{
							shape: '䷕',
							name: '贲',
							code: '100101'
						},{
							shape: '䷖',
							name: '剥',
							code: '100000'
						},{
							shape: '䷗',
							name: '复',
							code: '000001'
						},{
							shape: '䷘',
							name: '无妄',
							code: '111001'
						},{
							shape: '䷙',
							name: '大畜',
							code: '100111'
						},{
							shape: '䷚',
							name: '颐',
							code: '100001'
						},{
							shape: '䷛',
							name: '大过',
							code: '011110'
						},{
							shape: '䷜',
							name: '坎',
							code: '010010'
						},{
							shape: '䷝',
							name: '离',
							code: '101101'
					}]
				},{
				'title': '下经三十四卦',
				'lists': [{
					shape: '䷞',
					name: '咸',
					code: '011100'
				},{
					shape: '䷟',
					name: '恒',
					code: '001110'
				},{
					shape: '䷠',
					name: '遁',
					code: '111100'
				},{
					shape: '䷡',
					name: '大壮',
					code: '001111'
				},{
					shape: '䷢',
					name: '晋',
					code: '101000'
				},{
					shape: '䷣',
					name: '明夷',
					code: '000101'
				},{
					shape: '䷤',
					name: '家人',
					code: '110101'
				},{
					shape: '䷥',
					name: '睽',
					code: '101011'
				},{
					shape: '䷦',
					name: '蹇',
					code: '010100'
				},{
					shape: '䷧',
					name: '解',
					code: '001010'
				},{
					shape: '䷨',
					name: '损',
					code: '100011'
				},{
					shape: '䷩',
					name: '益',
					code: '110001'
				},{
					shape: '䷪',
					name: '夬',
					code: '011111'
				},{
					shape: '䷫',
					name: '姤',
					code: '111110'
				},{
					shape: '䷬',
					name: '萃',
					code: '011000'
				},{
					shape: '䷭',
					name: '升',
					code: '000110'
				},{
					shape: '䷮',
					name: '困',
					code: '011010'
				},{
					shape: '䷯',
					name: '井',
					code: '010110'
				},{
					shape: '䷰',
					name: '革',
					code: '011101'
				},{
					shape: '䷱',
					name: '鼎',
					code: '101110'
				},{
					shape: '䷲',
					name: '震',
					code: '001001'
				},{
					shape: '䷳',
					name: '艮',
					code: '100100'
				},{
					shape: '䷴',
					name: '渐',
					code: '110100'
				},{
					shape: '䷵',
					name: '归妹',
					code: '001011'
				},{
					shape: '䷶',
					name: '丰',
					code: '001101'
				},{
					shape: '䷷',
					name: '旅',
					code: '101100'
				},{
					shape: '䷸',
					name: '巽',
					code: '110110'
				},{
					shape: '䷹',
					name: '兑',
					code: '011011'
				},{
					shape: '䷺',
					name: '涣',
					code: '110010'
				},{
					shape: '䷻',
					name: '节',
					code: '010011'
				},{
					shape: '䷼',
					name: '中孚',
					code: '110011'
				},{
					shape: '䷽',
					name: '小过',
					code: '001100'
				},{
					shape: '䷾',
					name: '既济',
					code: '010101'
				},{
					shape: '䷿',
					name: '未济',
					code: '101010'
				}]
			}]}
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
	.title {
		font-size: 36rpx;
		line-height: 54rpx;
	}
	.gua-lists .shape {
		font-size: 96rpx;
		line-height: 120rpx;
		text-align: center;
	}
	.gua-lists .name {
		font-size: 64rpx;
		line-height: 80rpx;
		text-align: center;
	}
</style>
