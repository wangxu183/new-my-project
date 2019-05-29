<template>
  <div>
      <view class='Drad' @click="go()">
          <view class='dimo' >
              <img src="/static/tabs/fanfdajing.png"> 
              <p class="text">搜索资讯</p>
          </view>
        <img class="imga"  src="/static/tabs/whole.png">
      </view>
      <i-panel :title="title_name1"> 
        <ul  >
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