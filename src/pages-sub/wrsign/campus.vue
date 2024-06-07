<template>
  <view>
      <view class="layout">
         <view class="campus-block">
           <view v-for="item in 4 " class="campus-list">
             <view class="campus-item flex" @tap.stop="handleClass">
               <!-- #ifdef H5 -->
               <view class="cover radius-16">
                 <view class="h5-image cover radius-16"
                       :style="{ backgroundImage : `url('${campus.cover}')`}">
                 </view>
               </view>
               <!-- #endif -->
               <!-- #ifndef H5 -->
               <image mode="aspectFill" lazy-load class="cover radius-16" :src="campus.cover"></image>
               <!-- #endif -->
               <view class="flex-1 flex-between item-right">
                 <view class="pad">
                   <view style="padding: 10rpx;font-size: 32rpx">
                     <wd-icon name="home" color="#2e8eff"></wd-icon>
                     <span style="padding-left: 20rpx;font-weight: bold">{{campus.title}}</span>
                   </view>
                   <view style="padding: 10rpx;font-size: 30rpx">
                     <wd-icon name="location" color="#2e8eff"></wd-icon>
                     <span style="padding-left: 20rpx;font-size: 25rpx">{{campus.address}}</span>
                   </view>
                 </view>
                 <view>
                   <wd-icon name="arrow-right" size="22px" color="#2e8eff"></wd-icon>
                 </view>
               </view>
             </view>
           </view>
         </view>
      </view>
  </view>
</template>

<script setup lang="ts">


const campus = reactive({
    cover:'https://xyz.idot.work/attachment/image/666/23/08/1aca99f43e214faebf7a2f5d1c7c5ea1.png',
    title:"一手好字*尚云堂",
    address:"浙江省丽水市缙云县寺后路38号"
  })

const handleClass = () =>{
  uni.navigateTo({
    url:"/pages-sub/wrsign/class"
  })
}

</script>



<style scoped lang="scss">

.layout{
  .campus-block{
    .campus-list{
      position:relative;
      padding: 30rpx;
      background: #ffffff;
      .campus-item{
        box-shadow: 2px 2px 2px 1px rgba(0, 0, 255, .2);
        .cover{
          width: 180rpx;
          height: 180rpx;
        }
        .item-right{
          margin-left: 10rpx;
        }
      }
    }

  }
}

.radius-16{
  border-radius: 16rpx;
}
.h5-image {
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
}

</style>
