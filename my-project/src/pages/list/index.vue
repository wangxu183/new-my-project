<template>
  <div>
      <view class='Drad' @click="go()">
          <view class='dimo' >
              <img src="cloud://wangxu-44b924.7761-wangxu-44b924/images/fanfdajing.png"> 
              <p class="text">搜索资讯</p>
          </view>
        <img class="imga"  src="cloud://wangxu-44b924.7761-wangxu-44b924/images/whole.png">
      </view>
      <i-panel :title="title_name1"> 
        <ul  >
            <li class="box" @click="gone()">
            贵州，有生之年一定要去一次
             <p class="grad">2019-3-4 14:36:08</p>
            </li> 
            <li class="box" @click="gtwo()" >
            舌尖上的贵州那些不容错过的黔味美食
            <p class="grad">2019-3-4 14:36:08</p>
            </li> 
            <li class="box" @click="gthree()">
            贵州这十几个地方被全球推荐，2个地方进入前十！
             <p class="grad">2019-3-4 14:36:08</p>
            </li > 

            <li  class="box" @click="gfour()">
            贵州民族风俗
             <p class="grad">2019-3-4 14:36:08</p>
            </li> 
            <li  class="box" @click="gfive()">
            贵州乌江深处 百里画廊的秘密
             <p class="grad">2019-3-4 14:36:08</p>
            </li> 
          </ul>  
      </i-panel>
  </div>
</template>

<script>

export default {
    data : {
        value5: '',
        title_name1: "旅游动态",
      },
    onLoad (option){
     console.log(option.type)
    },
     methods: {
        go () {
       wx.navigateTo({
         url:('/pages/all/main')
       })
       console.log('type');
    },
        gone () {
       wx.navigateTo({
         url:('/pages/must/main')
       })
       console.log('all');
    },
      gtwo () {
       wx.navigateTo({
         url:('/pages/delicious/main')
       })
       console.log('delicious');
    },
      gthree () {
       wx.navigateTo({
         url:('/pages/feature/main')
       })
       console.log('type');
    },
      gfour () {
       wx.navigateTo({
         url:('/pages/spectial/main')
       })
       console.log('spectial');
    },

      gfive () {
       wx.navigateTo({
         url:('/pages/findnews1/main')
       })
       console.log('any');
    },
  },

}



</script>


<style scoped>

view.dimo {
    display: flex;
    width: 80%;
    background: #fff;
    flex-direction: row;
    border-radius: 10rpx;
    margin-right: 20rpx;
    margin-left: 20rpx;
}
view.dimo img {
    height: 42rpx;
    width: 42rpx;
    align-self: center;
    margin-left: 10rpx;
    margin-right: 20rpx;
}

view.dimo .text {
    flex: 1;
    font-size: 35rpx;
    color:#CDC0B0;
}
view.Drad {
    display: flex;
    flex-direction: row;
    height: 98rpx;
    background: #efeff4;
    align-items: center;
}
  ul{
   list-style:none;
   }
.grad{
    font-size:14px;
    color:#CDC0B0;
    padding-left:8px;
  }
  .imga{
    width:25px;
    height:25px;
    margin-left:20px;
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
</style>