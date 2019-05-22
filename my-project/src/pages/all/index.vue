<template>
  <div>
     <view class="Box"> 
        <i class="icon-search"></i>
        <input type="text" class="username" value="搜索"/>
     </view>
  
              <i-cell title="全部资讯" is-link></i-cell>
       
        
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
       
   
  },

}



</script>


<style scoped>
  ul{
   list-style:none;
   }

  .Box{
    width:390px;
    position: relative;
  }
 .icon-search {
    background: url('/static/tabs/fanfdajing.png') no-repeat;
    width: 30px;
    height: 50px;
    position: absolute;
    top: -1px;
    left: 0;
    }
.Box .username {
    padding-left: 30px;
    height: 25px;
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