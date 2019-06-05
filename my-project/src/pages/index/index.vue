<template>
  <div>
    <swiper
      indicator-dots="true"
      autoplay="true"
      interval="5000"
      duration="1000"
    >
      <block v-for=" item in imgUrls" :key="item">
          <swiper-item @click="transfor()" >
             <image class="img2" :src="item"/>
          </swiper-item>
      </block>
    </swiper>
  
    <i-grid i-class="no-border">
    <i-grid-item @click="changeone()" i-class="no-border">
        <i-grid-icon>
            <image src="cloud://wangxu-44b924.7761-wangxu-44b924/images/tour.png" />
        </i-grid-icon>
        <i-grid-label >景区推荐</i-grid-label>
    </i-grid-item>
    <i-grid-item @click="changetwo()" i-class="no-border">
        <i-grid-icon>
            <image src="cloud://wangxu-44b924.7761-wangxu-44b924/images/fun.png" />
        </i-grid-icon>
        <i-grid-label>民族风情</i-grid-label>
    </i-grid-item>
    <i-grid-item @click="changethree()" i-class="no-border">
        <i-grid-icon>
            <image src="cloud://wangxu-44b924.7761-wangxu-44b924/images/food.png" />
        </i-grid-icon>
        <i-grid-label>特色美食</i-grid-label>
    </i-grid-item>
    <i-grid-item @click="changefour()" i-class="no-border">
        <i-grid-icon>
            <image src="cloud://wangxu-44b924.7761-wangxu-44b924/images/play.png" />
        </i-grid-icon>
        <i-grid-label>旅游资讯</i-grid-label>
      </i-grid-item>
     </i-grid>
      <i-panel :title="title_name">         
            <view class="box1" @click="transfor()">
            <img class="imga" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/11.jpg">
            <p class="brad">贵州乌江深处：传统养峰蜕变观光旅游</p>
            <p class="grad">2019-3-4 14:36:08</p>
          </view>
          <view class="box1" @click="transfor()">
            <img class="imga" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/10.jpg">
            <p class="brad">贵州首条直升飞机低空旅游航线 暨航空物流港在凯里开工建设</p>
            <p class="grad">2017-7-04 09:02:58</p>
          </view>
          <view class="box1" @click="transfor()">
            <img class="imga" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/8.jpg">
            <p class="brad">贵州荔波发展全域旅游“实现生态美、百姓富”</p>
            <p class="grad">2018-6-25 18:06:34</p>
          </view>
          <view class="box1" @click="transfor()">
            <img class="imga" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/19.jpg">
            <p class="brad">一条渠作价3000万入股旅游公司 贵州中天集团探索金融扶贫</p>
            <p class="grad">2019-01-06 10:06:58</p>
          </view>
        </i-panel>
           <view>
      <ul @click="transfor()">
          <li>
            <h2 class="dimo1" >
              <img  class="img1" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/1.jpg">
            </h2>
            <h3 class="dimo">
              <img  class="img1" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/10.jpg">
            </h3>
          </li>
        </ul>
        <ul>
          <li>
            <h2 class="dimo1">
              <img  class="img1" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/18.jpg">
            </h2>
            <h3 class="dimo">
              <img  class="img1" src="cloud://wangxu-44b924.7761-wangxu-44b924/images/7.jpg">
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
            <p class="grad">2019-3-4 14:36:08</p>
            </li> 
            <li class="box">
            "文体旅"融合发展，贵州将办多项赛事
             <p class="grad">2019-3-4 14:36:08</p>
            </li > 
            <li class="box">
            贵州，有生之年一定要去一次
             <p class="grad">2019-3-4 14:36:08</p>
            </li> 
            <li  class="box">
            受降雨影响 贵州部分景区暂时关闭
             <p class="grad">2019-3-4 14:36:08</p>
            </li> 
            <li  class="box">
            2019国际山地旅游暨户外发展大会贵州站启动
             <p class="grad">2019-3-4 14:36:08</p>
            </li> 
          </ul>  
      </i-panel>
  
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
      'cloud://wangxu-44b924.7761-wangxu-44b924/images/t2.jpg',
      'cloud://wangxu-44b924.7761-wangxu-44b924/images/t12.jpg',
      'cloud://wangxu-44b924.7761-wangxu-44b924/images/05.jpg',
      'cloud://wangxu-44b924.7761-wangxu-44b924/images/t7.jpg'
    ],

      title_name: "旅游资讯",
      title_name1: "旅游动态",

      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    },
    

  components: {
    card
  },

  change: {
     
  },

  methods: {
   
    changeone () {
     wx.navigateTo({
         url:('/pages/fenews/main')
       })
       console.log('type1');
    },
    changetwo () {
     wx.navigateTo({
         url:('/pages/spnews/main')
       })
       console.log('type2');
    },
    changethree () {
     wx.navigateTo({
         url:('/pages/denews/main')
       })
      console.log('type3');
    },
    changefour () {
     wx.navigateTo({
         url:('/pages/list/main')
       })
      console.log('type4');
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
   width:175px;
   height:150px;
   margin-top:10px;
   margin-right:6px;
   margin-bottom:8px;
  }
  .dimo1{
    float:left;
    display:block;
    width:175px;
    height:150px;
    margin-left:8px;
    margin-top:10px;
    margin-bottom:8px;
  }

  .grad{
    font-size:14px;
    color:#CDC0B0;
    padding-left:8px;
  }
  .brad{
    font-size:15px;
    margin-top:8px;
    margin-right:5px;
  }
  .box1{
   display:block;
   width:380px;
   height:80px;
   border-bottom:1px solid #EEE9E9;
  }
   .imga{
     float:left;
     width:100px;
     height:70px;
     margin-top:4px;
     margin-left:8px;
     margin-right:8px;
     margin-bottom:10px;
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
  .img2{
    width:390px;
    height:180px;
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
