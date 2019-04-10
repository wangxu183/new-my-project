<template>
  <div >
   <i-tabs :current="current_scroll" scroll @change="handleChangeScroll">
    <i-tab key="tab1" title="选项1"></i-tab>
    <i-tab key="tab2" title="选项2"></i-tab>
    <i-tab key="tab3" title="选项3"></i-tab>
    <i-tab key="tab4" title="选项4"></i-tab>
    <i-tab key="tab5" title="选项5"></i-tab>
    <i-tab key="tab6" title="选项6"></i-tab>
    <i-tab key="tab7" title="选项7"></i-tab>
    <i-tab key="tab8" title="选项8"></i-tab>
    <i-tab key="tab9" title="选项9"></i-tab>
   </i-tabs>
    <view class="top-padding">
         <i-card title="西餐" extra="服务态度好" thumb="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1554136734498&di=4a94d72ac1a61ec76e83c1e5e6202629&imgtype=0&src=http%3A%2F%2Fimg1.qunarzz.com%2Fp%2Ftts6%2F1702%2Fa4%2Feac2c8a1e491e02.jpg_r_750x500x90_d537b527.jpg">
          <view slot="content">八分熟牛排</view>
          <view slot="footer">好是好吃，但是好贵</view>
         </i-card>
         <view class="top-padding"></view>
         <i-card title="马卡龙" extra="超级好吃" thumb="http://img1.imgtn.bdimg.com/it/u=2023513984,2730774655&fm=26&gp=0.jpg">
          <view slot="content">超级好看呢</view>
          <view slot="footer">一款超级好看还超级好吃的甜品</view>
         </i-card>
         <view class="top-padding"></view>
         <i-card title="榴莲" extra="水果之王" thumb="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1554137156969&di=d23f99f8475cabbabd7fb777c4b18413&imgtype=0&src=http%3A%2F%2Fbmp.skxox.com%2F201607%2F16%2Fbanghong520.112723.jpg">
          <view slot="content">超级好吃，还美容</view>
          <view slot="footer">就是脂肪含量很高，易发胖，不易吃多</view>
         </i-card>
        <view class="top-padding"></view>
         <i-card title="辣条" extra="就是挺喜欢吃的" thumb="http://img2.imgtn.bdimg.com/it/u=1535460409,2183749429&fm=26&gp=0.jpg">
          <view slot="content">辣条这个。。这个。。哈哈哈</view>
          <view slot="footer">最然喜欢吃，但是还是要少吃，毕竟不健康</view>
         </i-card>
          <view class="top-padding"></view>
      </view>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      current_scroll: 'tab1',
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    handleChange ({ detail }) {
      this.setData({
        current: detail.key
      })
    },
    handleChangeScroll (event) {
      this.current_scroll = event.mp.detail.key
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}
.all{
  width:7.5rem;
  height:1rem;
  background-color:blue;
}
.all:after{
  display:block;
  content:'';
  clear:both;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
