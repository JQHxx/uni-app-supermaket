<template>
	<view class="profile">
		<view class="header">
			<view class="yuan"></view>
			<view class="txt">
				<text class="txt1">注册/登录</text>
				<text class="txt2">暂无绑定手机号</text>
			</view>
			
		</view>
		<view class="content">
			<view>
				<text class="a">0.00</text>元
				<view>我的余额</view>
			</view>
			<view>
				<text class="a">0</text>个
				<view>我的优惠</view>
			</view>
			<view>
				<text class="a">0</text>分
				<view>我的积分</view>
			</view>
		</view>
		<view class="foot">
			<view v-for="item in row" class="zong">
				<view class="null">
				</view>
				<view class="row">
					{{item}}
				</view>
			</view>
		</view>
		<view class="zong">
			<view class="null">
			</view>
			<view class="row">
				我的购物车
			</view>
		</view>
		<view class="zong">
			<view class="null">
			</view>
			<view class="row">
				下载购物app
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return{
				row:["我的消息","积分商城","会员卡"],
				}
		}
	}
</script>

<style>
	.header{
		width: 100%;
		height: 160rpx;
		background-color: #ff8198;
		display: flex;
	}
	.yuan{
		width: 120rpx;
		height: 120rpx;
		border-radius: 50%;
		background-color: #FFFFFF;
		margin-left: 40rpx;
		margin-top: 20rpx;
	}
	.txt{
		display: flex;
		flex-direction: column;
		color: #FFFFFF;
		margin-top: 40rpx;
	}
	.txt1{
		font-size: 32rpx;
		padding-left: 20rpx;
	}
	.txt2{
		font-size: 28rpx;
		padding-left: 30rpx
	}
	.content{
		display: flex;
		width: 100%;
		height: 180rpx;
		background-color: rgb(215, 215, 215,0.4);
		justify-content: space-around;
		
	}
	.content>view{
		flex: 1;
		height: 160rpx;
		width: 30%;
		background-color: #FFFFFF;
		text-align: center;
	}
	.a{
		color: #FF5F3E;
		font-size: 20px;
		line-height: 90rpx;
	}
	.content>view view{
		font-size: 24rpx;
	}
	.foot{
		width: 100%;
		height: 280rpx;
		background-color: rgb(215, 215, 215,0.4);
	}
	.zong{
		display: flex;
		width: 100%;
		height: 88rpx;
	}
	.null{
		width: 10%;
		height: 88rpx;
		background-color: #FFFFFF;
	}
	.row{
		width: 90%;
		height: 88rpx;
		line-height: 88rpx;
		background-color: #FFFFFF;
		font-size: 28rpx;
		
	}
</style>