<template>
  <view class="layout">
    <scroll-view scroll-y	>
      <view class="container11">
          <view class="block">
            <view class="title flex-center">
              <view class="flex-center">
                <view class="line"></view>
                <view class="dot" style="margin-right: 12rpx"></view>
              </view>
              <view class="title-text">基本信息</view>
              <view class="flex-center">
                <view class="line"></view>
                <view class="dot" style="margin-left: 12rpx"></view>
              </view>
            </view>
            <view  class="items">
                <view class="card col-6">
                  <view class="field-name">区域</view>
                  <view class="field-val">缙云县青少年宫</view>
                </view>
                <view class="card col-6">
                  <view class="field-name">班级代码</view>
                  <view class="field-val">缙云县青少年宫</view>
                </view>
                <view class="card col-6">
                  <view class="field-name">状态</view>
                  <view class="field-val">报名进行中</view>
                </view>
              <view class="card col-6">
                <view class="field-name">学年</view>
                <view class="field-val">2024</view>
              </view>
              <view class="card col-6">
                <view class="field-name">学期</view>
                <view class="field-val">暑期</view>
              </view>
              <view class="card col-6">
                <view class="field-name">专业</view>
                <view class="field-val">少儿舞蹈</view>
              </view>
              <view class="card col-6">
                <view class="field-name">专业程度</view>
                <view class="field-val">启蒙</view>
              </view>
              <view class="card col-6">
                <view class="field-name">报名限制</view>
                <view class="field-val">学员年级段：幼儿 ～ 小学六年级</view>
              </view>
              <view class="card col-6">
                <view class="field-name">教师</view>
                <view class="field-val">陈老师</view>
              </view>
            </view>
          </view>

        <view class="block">
          <view class="title flex-center">
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-right: 12rpx"></view>
            </view>
            <view class="title-text">上课时间及地点</view>
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-left: 12rpx"></view>
            </view>
          </view>
          <view  class="items">
            <view class="card col-1">
              <view class="field-name">开课时间</view>
              <view class="field-val">2024-05-29</view>
            </view>
            <view class="card col-1">
              <view class="field-name">课表信息</view>
              <view class="field-val">周一、周三 18:30-20:00 少儿舞蹈教室</view>
            </view>
          </view>
        </view>


        <view class="block">
          <view class="title flex-center">
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-right: 12rpx"></view>
            </view>
            <view class="title-text">课程费用</view>
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-left: 12rpx"></view>
            </view>
          </view>
          <view  class="items">
            <view class="card col-6">
              <view class="field-name">课次</view>
              <view class="field-val">20</view>
            </view>
            <view class="card col-6">
              <view class="field-name">总费用</view>
              <view class="field-val">1000</view>
            </view>
          </view>
        </view>

        <view class="block">
          <view class="title flex-center">
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-right: 12rpx"></view>
            </view>
            <view class="title-text">费用明细</view>
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-left: 12rpx"></view>
            </view>
          </view>
          <view  class="items">
            <view class="card col-6">
              <view class="field-name">教学费</view>
              <view class="field-val">1000</view>
            </view>
          </view>
        </view>

        <view class="block">
          <view class="title flex-center">
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-right: 12rpx"></view>
            </view>
            <view class="title-text">班级描述</view>
            <view class="flex-center">
              <view class="line"></view>
              <view class="dot" style="margin-left: 12rpx"></view>
            </view>
          </view>
  <!--        <view  class="items">-->
  <!--          <view class="card col-6">-->
  <!--            <view class="field-name">区域</view>-->
  <!--            <view class="field-val">缙云县青少年宫</view>-->
  <!--          </view>-->
  <!--        </view>-->
        </view>

      </view>
    </scroll-view>

    <wd-button style="position: absolute;bottom: 0">主要按钮</wd-button>
  </view>
</template>

<script setup lang="ts">

</script>


<style scoped lang="scss">

.layout{
  padding:18rpx;
  .container11{
    padding:18rpx;
    .block{
      padding: .625rem;
      background-color: #fff;
      border-radius: .3125rem;
      margin-bottom: .625rem;
      box-shadow: 0 0 8px 1px #e8e8e8;

      .title{
        position: relative;
        .title-text{
          font-size: 36rpx;
          color: #222;
          font-weight: 700;
          display: inline-block;
          padding: 0 38rpx;
          background-color: #fff;
          position: relative;
          z-index: 10;
        }
      }

      .items{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        .card{
          background-color: #f8f8f8;
          border-radius: .3125rem;
          margin-top: 18rpx;
          padding: 18rpx;
          .field-name{
            font-size: .75rem;
            font-weight: 700;
            color: #222;
            padding-left: .75rem;
            position: relative;
            line-height: 1.25rem;
          }
          .field-name:before{
            content: "";
            display: block;
            width: .5rem;
            height: .5rem;
            background-color: #ffb03f;
            border-radius: 50%;
            position: absolute;
            top: .375rem;
            left: 0;
          }
          .field-val{
            font-size: 26rpx;
            color: #696571;
            padding-left: 24rpx;
          }
        }
        .card.col-6{
          width: calc(50% - 24px);
        }
        .card.col-1{
          width: 100%;
        }
      }
    }
  }
}

.dot{
  content: "";
  display: block;
  width: 16rpx;
  height: 16rpx;
  background-color: #3e7dfe;
  border-radius: 50%;
  z-index: 10;
}
.line{
  position: absolute;
  content: "";
  display: block;
  width: 60%;
  height: 1px;
  background-color: #f2f2f2;
}

</style>
