<template>
  <div>



    <swiper
      indicator-dots="{{indicatorDots}}"
      autoplay="{{autoplay}}"
      interval="{{interval}}"
      duration="{{duration}}"
    >
      <block v-for=" item in imgUrls" :key="item">
        <swiper-item>
          <image src="item" width="400" height="180" />
        </swiper-item>
      </block>
    </swiper>
  
    <i-grid i-class="no-border">
      <i-grid-item  i-class="no-border">
        <i-grid-icon>
            <image src="/static/tabs/dianzan.png" />
        </i-grid-icon>
        <i-grid-label>景区推荐</i-grid-label>
      </i-grid-item >  
      <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/tabs/wujiaoxing.png" />
        </i-grid-icon>
        <i-grid-label>民族风情</i-grid-label>
      </i-grid-item>
      <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/tabs/daocha.png" />
        </i-grid-icon>
        <i-grid-label>特色美食</i-grid-label>
      </i-grid-item>
     </i-grid>
     <i-grid i-class="no-border">
      <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/tabs/weixin.png" />
        </i-grid-icon>
        <i-grid-label>旅游资讯</i-grid-label>
      </i-grid-item>  
    </i-grid>
    <i-panel title="美食推荐">
      <view  v-for="item in candys" :key="item" class="top-padding">
         <i-card :title="item.name" :extra="item.intro" thumb="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1554136734498&di=4a94d72ac1a61ec76e83c1e5e6202629&imgtype=0&src=http%3A%2F%2Fimg1.qunarzz.com%2Fp%2Ftts6%2F1702%2Fa4%2Feac2c8a1e491e02.jpg_r_750x500x90_d537b527.jpg">
          <view slot="content">{{item.type}}</view>
          <view slot="footer">{{item.com}}</view>
         </i-card>
      </view>
    </i-panel>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      imgUrls: [
      'http://image.bestxinlv.com/xlly/RichImage/20190411163152733.jpg',
      'http://ly.xiaohongshu.wang/gz2-bd-p/images/t2.jpg',
      'http://www.gzcts09.com/uploads/allimg/180202/2-1P2021A3480-L.jpg'
    ],
    indicatorDots: false,
    autoplay: false,
    interval: 5000,
    duration: 1000,
      candys: [],
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
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },
  created () {
      this.$http.get('http://www.baidu.com', 'param').then((res)=>{
      console.log('res', res)
      }).catch(err=>{
      })
    const db = wx.cloud.database({ env: 'wangxu-44b924' })
    db.collection('candy').get().then(
      res => {
        console.log(res.data)
        this.candys = res.data
      }
    )
    wx.cloud.callFunction({ name: 'today' }).then(
      res => { console.log(res) }
    )
  }
}
</script>

<style scoped>
div >>> .no-border{
  border-width:  0pt;
}
div >>> .top-padding{
  padding-top:50rpx;
}

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
