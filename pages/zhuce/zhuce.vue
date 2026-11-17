<template>
  <view class="login-box">
    <!-- 顶部标题 -->
    <view class="top-title">
      <view class="logo">数字社区</view>
      <view class="big-text">欢迎登录，智慧社区</view>
      <view class="tip-text">连接社区服务，开启便捷数字生活</view>
    </view>

    <!-- 登录卡片 -->
    <view class="card">
      <input class="input" placeholder="请输入手机号" />
      <input class="input" placeholder="请输入密码" password />

      <view class="row">
        <text class="link">快速注册</text>
        <text class="link">忘记密码</text>
      </view>

      <button class="login-btn">登录</button>

      <view class="agree">
        <radio />
        <text>我已阅读并同意《用户隐私协议》</text>
      </view>
    </view>

    <view class="other-title">其他登录方式</view>
    <view class="login-row">
      <button class="other-btn">微信</button>
      <button class="other-btn">支付宝</button>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style scoped>
.login-box{
  padding: 40rpx;
  background-color: #f0f8f5;
  min-height: 100vh;
}
.top-title{
  margin-bottom: 60rpx;
}
.logo{
  font-size: 32rpx;
  margin-bottom: 20rpx;
}
.big-text{
  font-size: 56rpx;
  font-weight: bold;
  margin-bottom:16rpx;
}
.tip-text{
  color:#666;
  font-size:30rpx;
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
.row{
  display:flex;
  justify-content: space-between;
  margin:20rpx 0 40rpx;
}
.link{
  color:#389478;
  font-size:28rpx;
}
.login-btn{
  background: linear-gradient(90deg,#60c49e,#2b705b);
  color:#fff;
  border-radius:99rpx;
}
.agree{
  display:flex;
  align-items:center;
  margin-top:30rpx;
  font-size:28rpx;
  color:#555;
}
.other-title{
  text-align:center;
  margin:60rpx 0 40rpx;
  color:#999;
}
.login-row{
  display:flex;
  gap:30rpx;
}
.other-btn{
  flex:1;
  background:#fff;
  color:#333;
  border-radius:99rpx;
}
</style>
