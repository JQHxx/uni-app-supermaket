<template>
	<view class="goods" @click="native">
		<view class="goods-item" v-for="item in goods">
		<image :src="item.img || item.show.img"></image>
	      <view class="item-text">
	        <p>{{item.title}}</p>
	        <span class="price">{{item.price}}</span>
	        <span class="collect">{{item.cfav}}</span>
	      </view>
		</view>
	</view>
</template>

<script>
	export default {
		props :{
		        goods :{
		          type :Array,
		          default (){
		            return []
		          }
		        }
		      },
		methods:{
			native() {
				uni.navigateTo({
					url:'../../pages/detail/detail'
				})
			}
		}
	}
</script>

<style scoped>
	.goods{
		display: flex;
		flex-wrap:wrap;
		justify-content: space-around;
	}
  .goods-item {
    padding-bottom: 80rpx;
    position: relative;
    width: 48%;
  }

  .goods-item image {
    width: 100%;
    border-radius: 10rpx;
  }

  .item-text {
    font-size: 24rpx;
    position: absolute;
    bottom: 10rpx;
    left: 0;
    right: 0;
    overflow: hidden;
    text-align: center;
  }

  .item-text p {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    margin-bottom: 6rpx;
  }

  .item-text .price {
    color: var(--color-high-text);
    margin-right: 40rpx;
  }

  .item-text .collect {
    position: relative;
  }

  .item-text .collect::before {
    content: '';
    position: absolute;
    left: -30rpx;
    top: -2rpx;
    width: 28rpx;
    height: 28rpx;
    background: url("../../static/img/common/collect.png") 0 0/28rpx 28rpx;
  }
</style>
