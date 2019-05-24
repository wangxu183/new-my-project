<template>
  <div>
   <view class="userinfo">
    <view class="userinfo-avatar">
    <open-data type="userAvatarUrl"></open-data>
    </view>
    <open-data type="userNickName"></open-data>
   </view>
   <i-panel title="我想寻找的">
  <i-input :value="address" title="景区地址" autofocus placeholder="地址" />
  <i-input :value="name" title="景点名称"  placeholder="名称" />
  <i-input :value="reason" title="推荐原因"  placeholder="原因" />
  <i-button bind:click="handleClick">确认提交</i-button>
  </i-panel >
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data : {
       address:"",
       name:"",
       reason:"",
       movies:[  
        {url:'http://zsly01.qunar.wiki/gz_bd_p/images/t2.jpg'} ,  
        {url:'http://zsly01.qunar.wiki/gz_bd_p/images/t2.jpg'} ,  
        {url:'http://zsly01.qunar.wiki/gz_bd_p/images/t2.jpg'} ,  
        {url:'http://zsly01.qunar.wiki/gz_bd_p/images/t2.jpg'} 
        ]  
      },  
      onLoad: function () {  
      }, 
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
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
position: relative;
width: 750rpx;
height: 320rpx;
color: #666;
display: flex;
flex-direction: column;
align-items: center;
}
 
.userinfo-avatar {
overflow:hidden;
display: block;
width: 160rpx;
height: 160rpx;
margin: 20rpx;
margin-top: 50rpx;
border-radius: 50%;
border: 2px solid #fff;
box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
}

</style>
