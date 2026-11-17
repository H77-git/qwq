<template>
	<view class="home">

		<view class="zhaopian">
			<image class="image" src="/static/logo.png"></image>
		</view>
		<view class="dazi">
			<text class="zi">欢迎进入数字社区</text>
			<text class="ti">连接数字社区，开始便捷生活</text>
		</view>
		<view class="mian">
		<view class="wenzi">
			<text class="tip">数字社区</text>
			<text class="zzz">体验数字社区</text>
		</view>

		<view class="shuru">
			<input class="input" placeholder="输入账号" v-model="rop"/>
			<input class="input" placeholder="输入密码" v-model="plk"/>
		</view>

	<view class="denglu">
			<navigator url="/pages/denglu/denglu">
				<button class="dengru">注册</button>
			</navigator>
	<view class="zhuce">
		<button class="xingzhuche" @click="eee">登录</button>
	</view>
	</view>
		</view>
		<view class="dibu">
			<button @click="an">微信</button>
			<button>QQ</button>
		</view>

	</view>
</template>

<script>
export default{
	data(){
		return{
			rop:'',
			plk:''
		}
	},
	methods: {
		eee(){
			uni.navigateTo({
				url:'/pages/zhuce/zhuce'
			})
		},
		an(){
			uni.showToast({
				title:'没有这个功能',
				icon:'none'
			})
		}
	}
}
</script>

<style>
.mian{
	padding: 60rpx;
	background: wheat;
	border-radius: 60rpx;
}
.zhaopian{
	width: 600rpx;
	height: 350rpx;
	object-fit: cover;
	display: flex;
	justify-content: center;
	align-items: center;
	overflow:hidden;
	margin: 0 auto;
	box-shadow: 0 2rpx 10rpx #00000022;
	margin-bottom:30rpx
}
.image{
  width:600rpx;
  height:300rpx;
  object-fit:cover;

}
.home{
	padding: 20rpx;
}
.input{
	background-color:#475;
	border-radius: 16rpx;
	padding:24rpx;
	margin-bottom:24rpx;
	font-size:30rpx;
}
.shuru{
	align-items: center;
	border-radius: 16rpx;
}
.zzz{
	color: #666;
	font-size: 40rpx;
}
.tip{
	font-size: 60rpx;
	margin-bottom: 10rpx;
	font-weight: bold;
}
.wenzi{
	flex-direction: column;
	display: flex;
}
.dibu{
	display: flex;
	padding: 30rpx;
}
.dazi{
	margin-bottom:20rpx;
	display: flex;
	flex-direction: column;
}
.zi{
	font-weight: bold;
	margin-bottom: 20rpx;
	font-size: 40rpx;
}
.ti{
	color: #666;
	font-size: 30rpx;
}
</style>
