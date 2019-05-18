<template>
  <div>
      <i-panel :title="title_name1"> 
        <ul  >
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
</style>