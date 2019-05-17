<template>
  <div>
    <swiper
      :ndicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
    >
      <block v-for=" item in imgUrls" :key="item">
          <swiper-item>
             <image :src="item" width="420" height="300" />
          </swiper-item>
      </block>
    </swiper>
  
    <i-grid i-class="no-border">
      <i-grid-item @click="goType" v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
      </i-grid-item >  
     </i-grid>
     <div>
       <a href="#">
         <ul>
           <li> 
             <img src="/static/tabs/18.jpg" width="50" height="100" alt="#">
           </li>
            <li> 
             <img src="/static/tabs/14.jpg" width="50" height="100" alt="#">
           </li>
         </ul>
       </a>
     </div>
    <i-panel :title="title_name">
       <view class="top-padding">
         <i-card v-for="item in top" :key="item"  :extra="item.name1" :thumb="item.image">
          <view slot="content">{{item.name2}}</view>
          <view slot="footer">{{item.time}}</view>
         </i-card>
          <view class="top-padding"></view>
      </view>
   </i-panel>
      <button
        type="default"
        :size="defaultSize"
        :loading="loading"
        :plain="plain"
        :disabled="disabled"
        hover-class="other-button-hover"
      >
        查看更多
      </button>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
    data : {
        defaultSize: 'default',
        primarySize: 'default',
        warnSize: 'default',
        disabled: false,
        plain: false,
        loading: false,
      imgUrls: [
      'http://www.gzcts01.com//uploads/1489825451_4926.png',
      'http://www.gzcts01.com//uploads/image/1520587659_3283.png',
      'http://www.gzcts01.com//uploads/image/1520587659_4756.png'
    ],
    indicatorDots: false,
    autoplay: true,
    interval: 5000,
    duration: 1000,
      title_name: "旅游咨询",
      grids: [
        {title:"景区推荐",image:"/static/tabs/tour.png"},
        {title:"民族风情",image:"/static/tabs/fun.png"},
        {title:"特色美食",image:"/static/tabs/food.png"},
        {title:"旅游咨询",image:"/static/tabs/play.png"},
      ],
      top: [
         {name1:"贵州乌江深处",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"/static/tabs/wujiang.png"},
         {name1:"贵州乌江深处2",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"/static/tabs/wujiang.png"},
         {name1:"贵州乌江深处3",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"/static/tabs/wujiang.png"},
         {name1:"贵州乌江深处4",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"/static/tabs/wujiang.png"}
      ],
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
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
  button{
    font-size:15px;
    color:green;
  }
   ul{
   list-style:none;
   display:inline-block;
   }
   .clearfix::after{
    display:block;
    content:"";
    clear:both;
   }
   li{
     float:left;
   }
   a{
     text-decoration:none;
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
