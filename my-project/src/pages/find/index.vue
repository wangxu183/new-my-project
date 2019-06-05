<template>
  <div >
      <i-panel :title="title_name1">      
       <view class="top-padding" @click="revele()">
          <i-card v-for="item in top" :key="item"  :extra="item.name1" :thumb="item.image">
            <view slot="content">{{item.name2}}</view>
            <view slot="footer">{{item.time}}</view>
          </i-card>
            <view class="top-padding"></view>
        </view>
      </i-panel>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data : {
      title_name1: "旅游动态",
        top: [
         {name1:"贵州乌江深处",name2:"百里画廊的秘密",time:"2017-07-04 14:36:47",image:"cloud://wangxu-44b924.7761-wangxu-44b924/images/timg.jpg"},
         {name1:"贵州乌江深处2",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"cloud://wangxu-44b924.7761-wangxu-44b924/images/17.jpg"},
         {name1:"贵州乌江深处3",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"cloud://wangxu-44b924.7761-wangxu-44b924/images/15.jpg"},
         {name1:"贵州乌江深处4",name2:"传统养蜂蜕变观光旅游",time:"2017-07-04 14:36:47",image:"cloud://wangxu-44b924.7761-wangxu-44b924/images/14.jpg"},
      ],
  },
 
  components: {
    card
  },
   onLoad (option){
   console.log(option.type)
   },
  methods: {
       revele () {
       wx.navigateTo({
         url:('/pages/findnews1/main')
       })
       console.log('跳转');
    },
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
    .top-padding{
  padding-top:50rpx;
}

</style>
