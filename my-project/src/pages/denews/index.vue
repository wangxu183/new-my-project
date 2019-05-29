<template>
  <div>
     <view class="Drad" > 
       <view class="dimo" @click="go()">
        <img class="icon" src="/static/tabs/fanfdajing.png"  > 
         搜索资讯
      </view>
      <img class="imga" @click="go()" src="/static/tabs/whole.png">
     </view>
        <ul @click="wenttwo()" >
            <li class="box" >
             舌尖上的贵州那些不容错过的黔味美食
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
       wenttwo () {
       wx.navigateTo({
         url:('/pages/delicious/main')
       })
       console.log('switch');
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
  .text{
    font-size:10px;
  }
view.Drad {
    display: flex;
    flex-direction: row;
    height: 98rpx;
    background: #fff;
    align-items: center;
}

  .imga{
    width:25px;
    height:25px;
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
    background-color:#efeff4;
    margin-left:10px;
  }
  .icon{
    width:25px;
    height:25px;
    margin-top:5px;
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