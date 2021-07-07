<template>
	<view class="wrap">
			<u-row>
				<u-col span="6">
					<view>
						<view class="name">卦名: {{ info.name }}({{ info.pin_yin }})</view>
						<view class="shape">{{ info.shape }}</view>
					</view>
				</u-col>
				<u-col span="6">
					<view class="area">
						<view class="title">卦辞</view>
						<view class="ci">{{ info.gua_ci }}</view>
					</view>
					<view class="area">
						<view class="title">爻辞</view>
						<view class="yao" v-for="yao in info.yao_ci">
							{{ yao.kind }}: {{ yao.desc }}
						</view>
					</view>
				</u-col>
				<u-col span="12">
					<view class="area">
						<view class="title">大象</view>
						<view class="xiang">{{ info.da_xiang }}</view>
					</view>
					<view class="area">
						<view class="title">小象</view>
						<view class="xiang" v-for="xiang in info.xiao_xiang">
							{{ xiang.kind }}: {{ xiang.desc }}
						</view>
					</view>
				</u-col>
				<u-col span="12">
					<view class="area">
						<view class="title">彖辞</view>
						<view v-for="tuan in info.tuan_ci">
							{{ tuan }}
						</view>
					</view>
				</u-col>
			</u-row>
	</view>
</template>

<script>
export default {
	data() {
		return {
			info: {
				shape: '䷀',
				code: '111111',
				pin_yin: 'qián',
				name: '乾',
				gua_ci: '元、亨、利、貞。',
				yao_ci: [{
					kind: '初九',
					desc: '潜龙勿用。'
				},{
					kind: '九二',
					desc: '见龙在田，利见大人。'
				},{
					kind: '九三',
					desc: '君子终日乾乾，夕惕若；厉，无咎。'
				},{
					kind: '九四',
					desc: '或跃在渊，无咎。'
				},{
					kind: '九五',
					desc: '飞龙在天，利见大人。'
				},{
					kind: '上九',
					desc: '亢龙，有悔。'
				},{
					kind: '用九',
					desc: '见群龙无首，吉。'
				}],
				da_xiang: '天行健，君子以自强不息。',
				xiao_xiang: [{
					kind: '初九',
					desc: '潜龙勿用，阳在下也。'
				},{
					kind: '九二',
					desc: '见龙在田，德施普也。'
				},{
					kind: '九三',
					desc: '终日乾乾，反复道也。'
				},{
					kind: '九四',
					desc: '或跃在渊，进无咎也。'
				},{
					kind: '九五',
					desc: '飞龙在天，大人造也。'
				},{
					kind: '上九',
					desc: '亢龙有悔，盈不可久也。'
				},{
					kind: '用九',
					desc: '用九，天德不可为首也。'
				}],
				'tuan_ci': [
					'大哉乾元，萬物資始，乃統天。雲行雨施，品物流形，大明終始，六位時成。',
					'時乘六龍以御天，乾道變化，各正性命，保合大和〈一作太和〉，乃利貞。',
					'首出庶物，萬國咸寧。'
				]
			},
		}
	},
	onLoad(e) {
		this.info.yao_ci = this.info.yao_ci.reverse();
		this.info.xiao_xiang = this.info.xiao_xiang.reverse();
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
	.shape {
		color: red;
		font-size: 384rpx;
		line-height: 480rpx;
	}
	.name {
		font-size: 36rpx;
		text-align: center;
		line-height: 36rpx;
	}
	.xiang {
		color: blue;
	}
	.ci,.yao {
		color: red;
	}
	.area {
		padding: 5rpx 0;
		line-height: 45rpx;
		.title {
			font-weight: bold;
		}
	}
</style>
