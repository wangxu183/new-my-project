<template>
  <div>
    <swiper
      :ndicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
    >
      <block v-for=" item in imgUrls" :key="item">
          <swiper-item @click="transfor()" >
             <image :src="item" width="420" height="300" />
          </swiper-item>
      </block>
    </swiper>
  
    <i-grid i-class="no-border">
      <i-grid-item @click="change(grid)"  v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
      </i-grid-item >  
     </i-grid>
      <i-panel :title="title_name">
        <view class="top-padding">
          <i-card v-for="item in top" :key="item"  :extra="item.name1" :thumb="item.image">
            <view slot="content">{{item.name2}}</view>
            <view slot="footer">{{item.time}}</view>
          </i-card>
            <view class="top-padding"></view>
        </view>
    </i-panel>
           <view>
      <ul>
          <li>
            <h2 class="dimo1">
              <img  class="img1" src="/static/tabs/18.jpg">
            </h2>
            <h3 class="dimo">
              <img  class="img1" src="/static/tabs/1.jpg">
            </h3>
          </li>
        </ul>
        <ul>
          <li>
            <h2 class="dimo1">
              <img  class="img1" src="/static/tabs/10.jpg">
            </h2>
            <h3 class="dimo">
              <img  class="img1" src="/static/tabs/7.jpg">
            </h3>
          </li>
        </ul>
      </view>
      <button
        type="default"
        :size="defaultSize"
        :loading="loading"
        :plain="plain"
        :disabled="disabled"
        hover-class="other-button-hover"
        @click="refer()"
      >
        查看更多>>>
      </button> 
      <i-panel :title="title_name1"> 
        <ul @click="transfor()"  >
            <li class="box" >
            受降雨影响，贵州梵净山景区西线山门关闭
            <p>2019-3-4 14:36:08</p>
            </li> 
            <li class="box">
            "文体旅"融合发展，贵州将办多项赛事
             <p>2019-3-4 14:36:08</p>
            </li > 
            <li class="box">
            贵州，有生之年一定要去一次
             <p>2019-3-4 14:36:08</p>
            </li> 
            <li  class="box">
            受降雨影响 贵州部分景区暂时关闭
             <p>2019-3-4 14:36:08</p>
            </li> 
            <li  class="box">
            2019国际山地旅游暨户外发展大会贵州站启动
             <p>2019-3-4 14:36:08</p>
            </li> 
          </ul>  
      </i-panel>
  
      <button
        type="default"
        :size="defaultSize"
        :loading="loading"
        :plain="plain"
        :disabled="disabled"
        hover-class="other-button-hover"
        @click="transfor()"
      >
        查看更多>>>
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
      title_name: "旅游资讯",
      title_name1: "旅游动态",
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
    change(type){
    console.log('type')
    let url='../list/main?type=' + type.title
    mpvue.navigateTo({ url })
    },
      transfor () {
       wx.navigateTo({
         url:('/pages/list/main')
       })
       console.log('页面跳转');
    },
      refer () {
       wx.navigateTo({
         url:('/pages/list/main')
       })
       console.log('tiaozhuan');
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
  .dimo{
  float:right;
   display:block;
   width:184px;
   height:150px;
   margin-top:5px;
  }
  .dimo1{
    float:left;
    display:block;
    width:184px;
    height:150px;
    margin-left:4px;
    margin-top:5px;
  }
  p{
    font-size:14px;
    color:#CDC0B0;
    padding-left:8px;
  }
  .box{
    display:block;
    width:400px;
    height:50px;
    font-size:17px;
    padding-left:8px;
    padding-top:10px;
    border-bottom:2px solid #EEE9E9;
  }
  .img1{
    width:175px;
    height:150px;
    text-align:center;
  }
  button{
    font-size:15px;
    color:green;
  }
   ul{
   list-style:none;
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
