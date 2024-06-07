<template>
  <view class="layout">
    <view class="list">
      <scroll-view class="page-scroll" scroll-y style="height: 100%">
        <view v-for="item in 100">
          海报内容
        </view>
      </scroll-view>
    </view>
    <view class="sign-button">
      <wd-button block @click="handleSign">报名</wd-button>
    </view>
  </view>

</template>

<script setup lang="ts">

import useClipboard from "@/hooks/useClipboard";


const {setClipboardData} = useClipboard()

const handleSign = () =>{
  uni.navigateTo({
    url:"/pages-sub/wrsign/campus"
  })
}

</script>


<style scoped lang="scss">
.layout{
  display: flex;
  flex-direction: column;
  height: 100%;
  .list{
    flex: 1;
    position: relative;
    .page-scroll{
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
    }
  }
  .sign-button{
      position: absolute;
      bottom: 10rpx;
      width: 100%;
  }
}

</style>
