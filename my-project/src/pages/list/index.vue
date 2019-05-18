<template>
  <div>
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
          <view class="box1">
            <img class="imga" src="/static/tabs/16.png">
            <p class="brad">贵州乌江深处：传统养峰蜕变观光旅游</p>
            <p class="grad">2019-3-4 14:36:08</p>
          </view>
          <view class="box1">
            <img class="imga" src="/static/tabs/10.jpg">
            <p class="brad">贵州首条直升飞机低空旅游航线 暨航空物流港在凯里开工建设</p>
            <p class="grad">2017-7-04 09:02:58</p>
          </view>
          <view class="box1">
            <img class="imga" src="/static/tabs/16.png">
            <p class="brad">贵州荔波发展全域旅游“实现生态美、百姓富”</p>
            <p class="grad">2018-6-25 18:06:34</p>
          </view>
          <view class="box1">
            <img class="imga" src="/static/tabs/16.png">
            <p class="brad">一条渠作价3000万入股旅游公司 贵州中天集团探索金融扶贫</p>
            <p class="grad">2019-01-06 10:06:58</p>
          </view>
      </i-panel>
  </div>
</template>

<script>

export default {
    data : {
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
</style>