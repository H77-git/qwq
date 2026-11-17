<template>
	<view class="register">
		<!-- 返回箭头 + 标题 -->
		<view class="header">
			<view class="back" @click="goBack">←</view>
			<view class="title">注册账号</view>
		</view>

		<!-- 顶部文字 -->
		<view class="top-text">
			<view class="big">创建社区账号</view>
			<view class="tip">注册信息提交后需经社区管理员审批</view>
		</view>

		<!-- 卡片 -->
		<view class="card">
			<input class="input" placeholder="请输入手机号" v-model="phone"/>

			<view class="code-row">
				<input class="input code-input" placeholder="请输入验证码" v-model="code"/>
				<view class="get-code" @click="getCode">获取验证码</view>
			</view>

			<input class="input" placeholder="请输入密码（6-20位）" password v-model="pwd"/>
			<input class="input" placeholder="请输入姓名" v-model="name"/>
			<input class="input" placeholder="请输入身份证号" v-model="idCard"/>

			<view class="agree">
				<radio v-model="isAgree" />
				<text>我已阅读并同意《用户服务协议》</text>
			</view>

			<button class="reg-btn" @click="submit">注册</button>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			phone: '',
			code: '',
			pwd: '',
			name: '',
			idCard: '',
			isAgree: false
		}
	},
	methods: {
		goBack(){
			// 返回上一页
			uni.navigateBack()
		},
		getCode(){
			uni.showToast({
				title:"验证码已发送",
				icon:"none"
			})
		},
		submit(){
			uni.showToast({
				title:"提交成功，等待审核",
				icon:"success"
			})
		}
	}
}
</script>

<style scoped>
.register{
	padding: 40rpx;
	background-color: #f0f8f5;
	min-height: 100vh;
}
.header{
	display:flex;
	align-items:center;
	position:relative;
	margin-bottom:60rpx;
}
.back{
	width:60rpx;
	height:60rpx;
	background:#fff;
	border-radius:50%;
	display:flex;
	align-items:center;
	justify-content:center;
	font-size:32rpx;
}
.title{
	position:absolute;
	left:50%;
	transform:translateX(-50%);
	font-size:34rpx;
	font-weight:bold;
}
.top-text{
	margin-bottom:40rpx;
}
.big{
	font-size:52rpx;
	font-weight:bold;
	margin-bottom:16rpx;
}
.tip{
	color:#666;
	font-size:28rpx;
}
.card{
	background:#fff;
	border-radius:24rpx;
	padding:40rpx;
}
.input{
	background:#f6f9f8;
	border-radius:16rpx;
	padding:24rpx;
	margin-bottom:24rpx;
	font-size:30rpx;
}
.code-row{
	display:flex;
	align-items:center;
	background:#f6f9f8;
	border-radius:16rpx;
	margin-bottom:24rpx;
}
.code-input{
	flex:1;
	margin-bottom:0;
	background:transparent;
}
.get-code{
	padding:0 24rpx;
	color:#389478;
	font-size:28rpx;
}
.agree{
	display:flex;
	align-items:center;
	margin:20rpx 0 40rpx;
	font-size:28rpx;
	color:#555;
}
.reg-btn{
	background: linear-gradient(90deg,#60c49e,#2b705b);
	color:#fff;
	border-radius:99rpx;
}
</style>
