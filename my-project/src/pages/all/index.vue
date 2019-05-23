<template>
  <div>
          <view class='Drad'>
              <view class='dimo'>
                  <img src="/static/tabs/fanfdajing.png"> 
                  <input placeholder='站内查询'>
              </view>
          </view>
              <i-cell title="全部资讯" @click="go()" is-link></i-cell>
              <i-cell title="默认分类" is-link></i-cell>
              <i-cell title="旅游资讯" is-link></i-cell>
             <i-cell title="贵州印象" is-link></i-cell>
             <i-cell title="新闻" is-link></i-cell>
             <i-cell title="民族风情" is-link></i-cell>
              <i-cell title="特色美食" is-link></i-cell>
              <i-cell title="景区推荐" is-link></i-cell>
       
       

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
         url:('/pages/find/main')
       })
       console.log('type');
    },
   
  },

}



</script>


<style scoped>

view.dimo {
    display: flex;
    width: 100%;
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

view.dimo input {
    flex: 1;
    font-size: 30rpx;
}
view.Drad {
    display: flex;
    flex-direction: row;
    height: 98rpx;
    background: #efeff4;
    align-items: center;
}

</style>