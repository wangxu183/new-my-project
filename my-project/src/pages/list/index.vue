<template>
  <div>
     <view class="Drad" @click="go()"> 
       <view class="dimo">
        <img class="icon" src="/static/tabs/fanfdajing.png"> 
        搜索资讯
      </view>
      <img class="imga" src="/static/tabs/whole.png">
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
        defaultSize: 'default',
        primarySize: 'default',
        warnSize: 'default',
        disabled: false,
        plain: false,
        loading: false,
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
  ul{
   list-style:none;
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
  .Drad{
    width:390px;
    height:35px;
  }
  .imga{
    width:30px;
    height:30px;
    margin-left:20px;
  }
  .crad{
    font-size:14px;
    padding-left:8px;
  }
  .dimo{
    float:left;
    width:290px;
    height:30px;
    text-align:center;
    background-color:#e6e6e6;
    border:1px solid #EEE9E9;
    margin-left:10px;
  }
  .icon{
    width:25px;
    height:25px;
    margin-top:2px;
    color:#EEE9E9;
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