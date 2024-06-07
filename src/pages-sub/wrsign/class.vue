<template>
  <view class="layout">
      <view class="clazz">
        <view class="class-list" v-for="item in 5">
          <view class="class-item" @tap.stop="handleClass">
            <view class="flex flex-between">
              <view style="font-weight: 700;font-size: 32rpx;color:#3f3965">{{clazz.title}}</view>
              <span class="status">
                <img style="height: 28rpx" alt="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABUAAAAYCAYAAAAVibZIAAACw0lEQVQ4jY2UW4hOURTHf2d8TVMuDU0RImG8zPCA3DO5lUmiSUZepNxLIi/kcZ5QLinEk1J4YOR+y10NkpHEUDRmhnGZa3P7zj5L62tNs32+74x/7c46e6+99lrrv9ZCROLWHhHpFJFWEfkuIs0i0iUiR+LuJUCIwWggz9ZgT21c3CWiKOxv5UVRWBFFoURReNr+Y+8kIIp9FOgCck3Otf9YBJHrznQeAJuAlcCSDOcPgUvACaDjn8vOpfaKgFPAUeATcNbLWw/wGPgGDANmA0Ps7Aew1uQKYDfwIIGkwi8BZtjqxTXgAPDLSEoAIdBuRrcC5cAt706pGg3CsLV34zawyOQ1emjfLcAE72ItcBI4Y/t3bL8amJIKP0w2YT/3gXxgGtAIvE0ro0xQ3QagzghUDm4EyaRGx3ugENgGHAdcfwx70FouBq4DLepYkOxpnA5U2YsjgY/A+BgjzipjGbAC6AQGAk+BmcCqoKe74ZglfT3wBbgbY/AcsBNoshQN8jioNx4u5ghuquAQXJXglpqcvl4JrkRw5YKrF9w7wQ3ydMoE12hyUQJxBfbaAMtrOnQ4zLEwFduBsWk6kz2vhydEnE9KNoLGGJkjgMMZzpP09bskRMJaz8PXVhY+AuuoK8DiLI8+A9pM/pqDhM+QECQsRcJKk9NXARKuQ8JRWc7PI2Gxyc+DjvbqQgut2+amdsjCLB5lQo1F+tlyXaLhf7BSmA8cslb9DQz9T6NqcIcZrEn1fnub1n2q6OtMaaNNrJsxOVS8ABYA84CrtqdV8EY9xQp3OXDZhsUkYDUwVzvEpli+Tagn1gT3rLP2m8ENalCFoK3lkf96GXDBGNc+3mvtp2OvF1o+Okj2WakpNtvATiFobdbh9Bd0nB00z338NG/9B5SLXcBLXzFoac7a6rPMc03BRCNOa1HJ0Lqs9GZpH4A/THiJfr0OWnEAAAAASUVORK5CYII="/>
                <span style="padding-left: 10rpx">报名进行中</span></span>
            </view>
            <view class="flex flex-between row-year">
              <view>年份：2024</view>
              <view>|</view>
              <view>学期：暑期</view>
              <view>|</view>
              <view><span style="font-weight:700;color:#f77644">￥500</span> &nbsp;元 </view>
            </view>
            <view class="flex flex-center" style="margin-top: 12rpx">
              <!-- #ifdef H5 -->
              <view class="cover radius-16">
                <view class="h5-image cover radius-16"
                      :style="{ backgroundImage : `url('${clazz.cover}')`}">
                </view>
              </view>
              <!-- #endif -->
              <!-- #ifndef H5 -->
              <image mode="aspectFill" lazy-load class="cover radius-16" :src="clazz.cover"></image>
              <!-- #endif -->
              <view class="flex-1  item-right">
                <view class="row">
                  <view class="field area">区域：缙云县青少年宫</view>
<!--                  <view>区域：缙云县青少年宫</view>-->
                </view>
                <view class="row">
                  <view class="field classname">声乐</view>
                </view>
               <view class="row">
                 <view class="field time">周二 19:15-20:15 声乐小组课</view>
               </view>
                <view class="row">
                  <view class="field grade">学员年级段：幼儿 ～ 小学六年级</view>
                </view>
              </view>
              </view>
          </view>
        </view>
      </view>

  </view>
</template>

<script setup lang="ts">

const clazz = reactive({
  cover:'https://xyz.idot.work/attachment/image/666/23/08/1aca99f43e214faebf7a2f5d1c7c5ea1.png',
  title:"周二声乐小组（中大班）",
  address:"浙江省丽水市缙云县寺后路38号"
})
const handleClass = () =>{
  uni.navigateTo({
    url:"/pages-sub/wrsign/course_detail"
  })
}

</script>



<style scoped lang="scss">

.class-list{
  position:relative;
  padding: 30rpx;
  background: #ffffff;
  .class-item{
    box-shadow: 2px 2px 2px 1px rgba(0, 0, 255, .2);
    .cover{
      width: 180rpx;
      height: 180rpx;
    }
    .item-right{
      margin-left: 20rpx;
    }
  }
}

:root {
  --ion-color-button-tradient-from: #5ab1fa;
  --ion-color-primary:#3e7dfe
}

.status{
  display: flex;
  height: 2rpx;
  line-height: 10rpx;
  padding: 30rpx;
  background: linear-gradient(180deg, #5ab1fa, #3e7dfe);
  border-radius: 30rpx;
  color: #fff;
  font-size: 24rpx;
  align-items: center;
  white-space: nowrap;
  margin-right: 30rpx;
}

.radius-16{
  border-radius: 16rpx;
}
.h5-image {
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
}

.row-year{
  line-height: 60rpx;
  background-color: #f8f8f8;
  border-radius: 10rpx;
  padding: 8rpx;
  margin-right: 20rpx;
  margin-top: 20rpx;
  font-size: 28rpx;
  color: #696571;
  display: flex;
  justify-content: space-between;
}


.item-right{
  .row {
      position: relative;
      font-size: 26rpx;
      margin: 12px;
      .field{
        padding-left: 1.25rem;
      }
     .field:before {
        position: absolute;
        left: 0;
        top: 10%;
        //margin-top: -.46875rem;
       //margin-top: 10rpx;

       content: "";
        display: block;
        width: .9375rem;
        height: .9375rem;
        background-size: auto 100%;
        background-repeat: no-repeat;
    }
    .area{
      color:#e6a23c
    }
    .field.area:before {
      background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABkAAAAdCAYAAABfeMd1AAADXUlEQVRIiZ2WW4hWVRTHf/tjBpoeDjVJxnRFrB6cGVGKkOyibvNpBkQkBf3kAxGFEaEgoocCKQJ96qXEHorUwAsOpPNgbs1CRUF8UPHBTMg0vDa1BxxFmSPL+Z/h+M053zf2fzn7stb6r733uhxHA6Q+eQpYDMwHZgIvABVgBLgInAT2AztdiDfLLBWSpD5pBz4FVgFtjRwRhoHNwHoX4j9NSVKfmNdbgMm55SvAb8B5YBB4EpgKvA08k5O7Cix3Ie4vJUl9UgW+05UYjph3QHAhjhQ4ZHJep35TyyZXcyH+MI4k9Ukv0C+Cu8A6YJMLMW12V6lPzM5q4CugVUQLXYg/jZGkPnkWOAM8IYIeF+K+ZsYLyBYAe0T0L9DpQrycXctGERj6/g/BA49H9fo0NXsbHqynPnkJuKBT/eJCnNvA06eBDuBvF+K1BnIHgTk2BKa0AMtybzOQ+qQHuA1EwAxdUn58K8XM0CFgpQvxjwKeLyVrdpfZdc3Thhn8XePHAPO6E3gfOJYnEN616NN71uOAwtkwz0i6NTmh49VjKTBJaz+qAmzV3HLpk4K3GZFjhm4jadfkcskVZ078CXwD7AaqikZD2Rte1Le9UiJQBnPoVe01zZ8MLbky0VEiYx4/B7wIrAWOAhaRXdr/tUTveX0HK7ljv15SMHcA/2mclZCq5teBz+sVVAFmZU5WFAkomqYUkNwAPgZO161bCL/lQrxUoPNOrsAGS0arpud0isNZlpZgkt7lpgvx+zKh1CdBqWHv9nLFhWjle7v2ZwNvNCC5IYdKG1Tqk1ou97ZbsmbR9REwpPGH6hWPjNQnFs5fS29Idkf7hgvxL2CFSrRl+xfAKw1IhgtOYM1ur/TNzgrZHWtORtSfq6Btqj/TSkiu1xFYLxrIteo+2eMhEhFZRtfkSau64owCkiybjWAJsCvXrGqyM4ZxGa+osTy4J8XPgNdyIldciIMisAq+TXImXy2KusKy4kI0xUXqkhUl4Gy1gFMiWKMfjqxdL5LeOJTWLvXn3twjW6RMdyHeSX3yQS6KbL836+eFtso2MigsrW8/riVrsQs0vqX/gYONbDQlYZTIEvRnIMktW+d8z4V4vJn+hEq9DFlxtIw32NdPhOCRkfqkK/XJWftOWBm4D0dqCs2DNNTwAAAAAElFTkSuQmCC);
    }
    .field.classname:before {
      background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAAaCAYAAABctMd+AAABbklEQVRIieWWPUvDQBjHfxdrwaqnky9QFEEQKYiLg4uoHOhXcPdrOLr4IRzddXHJIuLkIthNoZMvqCBErXaoJydPJC1tEk108Q8H4bnnfnle7i5RANboCrANrAKD5KMDZY2eB46BgZygXyoAOwK2wC5QTVhTBPrbbA2gLs/rwBoCXxHjnvKDzaRorNFjwEKbuab8oCrzwyHckxc4XaZNN628vIFR/U/4E3AX51CIm+yiADgDboAmMA685gJXflCP7Gmn626+v9rQaOQla/Q00CuntSF1fVR+0MwKLwOzHXya1ugr4EJKklppytIDTLhrwmVmje66xhrtgh3tFHmSPMls0hpdk2344nosF5+DTgFDP4GHKgEVGbH6s90yJ00tZmSWO8ET0/yu2mt+CzxkZI7IaIGfA1vAe0b4hozPhoan7z4HcItc5CfAErAMvMVdRCk1E/q5Xwv3sT0C+vKM2slTfnAKLAKHwHNuZNj/AK7aTJNUDyM1AAAAAElFTkSuQmCC)
    }
    .field.time:before {
      background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABsAAAAbCAYAAACN1PRVAAAC3ElEQVRIib2WQUgVURSGvxmlMmyiFkmBKbhrkwURUSrYLNrUSkRI2lnpokXRKkiEaCMJBWnoohAXJe2i3djitbAIIpctDEWQkgiaRKXSGwf+ydfw3ryxoB/mnTv33nP+d87ce87xqAAXBnVAJ9AONAP1QBWwDiwA74AXwKQXxZ+yrJUlc2HQAAwA3TJeCUY+AfR7UTyfm8yFwWVgCKjR1E+goGcWWAZqgSagVU+19q4CV70ofpBJ5sLAPBgBejS1AgwCw14UL2VEYR/QB1wHdmp6DOj1oni9nNKoCwOn55ULg8YSey65MFgzWWKtUXqJjdHidT8VusSjZxYaL4rnSvynM8B2yT+g/a3SN/TI7iaZDsOQ5l4DHV4Ufy8TNS8l04Sm1yE7hiHZ/+3ZgA6DfaOuDKJckH6X7NXIPr7uUbeMDJYJ3d8QzulwGbqNp1oXtkrHe0Qn0jx2wIYXxRv/wDkM3NC16LSf01qYBo6VuA5rwEdg3ovieIveLbkwKCj7tJsHh7X2tswl3wHYFWhzYXAOaNF8iwuDphycBclmX7nOsJhD8TawV2OTD3PozErW+0V5by2HYtqTozl0liWrfCVQFK5KeF/GUBZqtbbuq0wYDuRQvKuS8kPvdS4MzlfQSaKxYGQzeskTks/ATV2XD5q778LgYIZOq+SMkU3p5QSwKwchCv0dwDLFbmDchYGf3qRqkJBN2YZJKVcXHes8sPA/0r424FoJnT7ZNfuTvkr5hBYvAHu2QPgceKPxLRcGh4q8alB9M0wYT+J6vyqsFb4rRVW3EpzC+QXYpk9hRDZ+Inursr+ZMVR3RpL42odXvqyEFaWzU0WX/ClwVuPepEVI58HRogJq6eue/nUWvnpRXJC+pbXHwHHtH/Oi+GKim6cHGQdeAt/KEC4o1VXsQbbSXU3L20WlNss4+4EjwMktd1cpwv/TN6ZIk47Y6p6Vo3RHbBnIDlR2Rwz8AgqWAG2+SQLfAAAAAElFTkSuQmCC)
    }
    .field.grade:before {
      background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAADJUlEQVRIiaWWWajPQRTHP3PtYsolIkv2patEWR+UBoUHW6Esb7ZQQlJIkaQkrj2SF0+EyANjC6WLZHmUsouIsXMZnetcjf/9/f7/K6em38zZvnPOnDnz418oOjstOvtIx7R/sTX1UYrOdgF2AeMKRKeBhcaHh/8FFJ1tCCwB1gPNlf1Mvx30+wlYA2w3PlTn+SorAjIIqAK2KEgEdgJ9dexUXnPVqVKb+kUUnW2hESxJNnIXmGt8uFagOxTYB/RX1k+JTCI0PnzIBYrOTtCz6KSsz8B+4DzwSgCND6HAphGwDFgLNFP2Yz27U38BRWfb606mJk6uAAeA1wnvB3DD+PAyIxPdgT2AS9hHJDPGh+cmOjtT821VKI53ADezcg18By4bHz5mCdXfVqCNst4DSwXoY1JRVaqU6SQhSd/VvCqLzrYGTgAjlPW1TPNfS4OByQlwHkn0Q6KzTTJAWgGbEhCh2xKRgC0ENgItVfBK03erBKCk8T7w1PjwOTo7HdgGtE3Sdlgu9p+qi8521IKYlDi6BBwE3pQALAdmA6MS3jFgBdCPnHs0EagEOipLSnyvgv4oUG8AjATmJaX9BFhsfDgenW0KjM4EUjA5gw3AokTnHrBb7wh61xYAFbVmmu7VcvhAQ91YDVCdFhSdXQUMND5IZ5Cbf0dFFRrpFB2VCYjoDFWbgbrumfrN6nW9gQvR2Y3GByl36V8rNYWiP0dHmfJENkh0o7NDxBboVeg0t6kCw2ty60O18WGz7v5MIpd5hciS+9Qs29XvPBbSN12Xp3zjwwNgbHR2jK7PZNi2SOZBm6xQdRbQC/12jc42Nj58S4U5ALXUJ5k/E9vo7Fkpiiygy8nuxgInizgupMm6lsb7RTdW8806o4tJx16nr2xJis6OB4ap3tFC/TpAxgdpK5t1KaVaGZ0t9eRLlR3S5Wt9LooDKUkHv67z+YDc8s4ZANIrZwDy8rau1Tc+vK0TQJFdtgN8cimlKM5J/rVZSmeQdHVLzJYbH+T/oQ6VSom0InkU5TErRlKpC6S/5SnV979uADBLI+ihzfSdpkwO/nDei1tDwC/7vAsFtcxRGQAAAABJRU5ErkJggg==)
    }
  }
}

.area-icon{
  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABkAAAAdCAYAAABfeMd1AAADXUlEQVRIiZ2WW4hWVRTHf/tjBpoeDjVJxnRFrB6cGVGKkOyibvNpBkQkBf3kAxGFEaEgoocCKQJ96qXEHorUwAsOpPNgbs1CRUF8UPHBTMg0vDa1BxxFmSPL+Z/h+M053zf2fzn7stb6r733uhxHA6Q+eQpYDMwHZgIvABVgBLgInAT2AztdiDfLLBWSpD5pBz4FVgFtjRwRhoHNwHoX4j9NSVKfmNdbgMm55SvAb8B5YBB4EpgKvA08k5O7Cix3Ie4vJUl9UgW+05UYjph3QHAhjhQ4ZHJep35TyyZXcyH+MI4k9Ukv0C+Cu8A6YJMLMW12V6lPzM5q4CugVUQLXYg/jZGkPnkWOAM8IYIeF+K+ZsYLyBYAe0T0L9DpQrycXctGERj6/g/BA49H9fo0NXsbHqynPnkJuKBT/eJCnNvA06eBDuBvF+K1BnIHgTk2BKa0AMtybzOQ+qQHuA1EwAxdUn58K8XM0CFgpQvxjwKeLyVrdpfZdc3Thhn8XePHAPO6E3gfOJYnEN616NN71uOAwtkwz0i6NTmh49VjKTBJaz+qAmzV3HLpk4K3GZFjhm4jadfkcskVZ078CXwD7AaqikZD2Rte1Le9UiJQBnPoVe01zZ8MLbky0VEiYx4/B7wIrAWOAhaRXdr/tUTveX0HK7ljv15SMHcA/2mclZCq5teBz+sVVAFmZU5WFAkomqYUkNwAPgZO161bCL/lQrxUoPNOrsAGS0arpud0isNZlpZgkt7lpgvx+zKh1CdBqWHv9nLFhWjle7v2ZwNvNCC5IYdKG1Tqk1ou97ZbsmbR9REwpPGH6hWPjNQnFs5fS29Idkf7hgvxL2CFSrRl+xfAKw1IhgtOYM1ur/TNzgrZHWtORtSfq6Btqj/TSkiu1xFYLxrIteo+2eMhEhFZRtfkSau64owCkiybjWAJsCvXrGqyM4ZxGa+osTy4J8XPgNdyIldciIMisAq+TXImXy2KusKy4kI0xUXqkhUl4Gy1gFMiWKMfjqxdL5LeOJTWLvXn3twjW6RMdyHeSX3yQS6KbL836+eFtso2MigsrW8/riVrsQs0vqX/gYONbDQlYZTIEvRnIMktW+d8z4V4vJn+hEq9DFlxtIw32NdPhOCRkfqkK/XJWftOWBm4D0dqCs2DNNTwAAAAAElFTkSuQmCC);

}

</style>
