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
						<view class="ci" v-for="gua,index in info.gua_ci" :key="index">{{ gua }}</view>
					</view>
					<view class="area">
						<view class="title">爻辞</view>
						<view class="yao" v-for="(yao, index) in info.yao_ci" :key="index">
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
						<view class="xiang" v-for="xiang, index in info.xiao_xiang" :key="index">
							{{ xiang.kind }}: {{ xiang.desc }}
						</view>
					</view>
				</u-col>
				<u-col span="12">
					<view class="area">
						<view class="title">彖辞</view>
						<view v-for="tuan, index in info.tuan_ci" :key="index">
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
				shape: '',
				code: '',
				pin_yin: '',
				name: '',
				gua_ci: '',
				yao_ci: [],
				da_xiang: '',
				xiao_xiang: [],
				'tuan_ci': []
			},
		}
	},
	onLoad(e) {
		this.loadData(e)
	},
	onReachBottom(e){
	},
	methods:{
		loadData(e){
			const data = require('@/static/gua/' + e.code + '.json')
			this.info	=  data;
			console.log(data)
			this.info.yao_ci = this.info.yao_ci.reverse()
			this.info.xiao_xiang = this.info.xiao_xiang.reverse()
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
