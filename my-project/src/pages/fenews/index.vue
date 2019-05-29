<template>
  <div>
      <view class='Drad' @click="go()">
          <view class='dimo' >
              <img src="/static/tabs/fanfdajing.png"> 
              <p class="text">搜索资讯</p>
          </view>
        <img class="imga"  src="/static/tabs/whole.png">
      </view>
        <ul @click="went()" >
            <li class="box" >
             贵州这十几个地方被全球推荐，2个地方进入前十
            <p class="grad">2019-2-6 14:36:08</p>
            </li> 
          </ul>  
  </div>
</template>

<script>

export default {
    data : {
      
        
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
       went () {
       wx.navigateTo({
         url:('/pages/feature/main')
       })
       console.log('switch');
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