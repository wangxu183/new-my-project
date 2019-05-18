<template>
  <div >
      <i-panel :title="title_name1"> 
        <ul>
            <li class="box" >
            时光贵州印象
            <p>2017-2-5 09:12:08</p>
            </li> 
            <li class="box">
            舌尖上的贵州 那些不容错过的黔味美食
             <p>2018-8-24 10:34:08</p>
            </li > 
            <li class="box">
            贵州民族风俗
             <p>2018-9-4 11:20:56</p>
            </li> 
            <li  class="box">
            贵州这11个地方被全球推荐 2个地方进入前十
             <p>2018-1-23 16:45:52</p>
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
import card from '@/components/card'

export default {
  data : {
      title_name1: "旅游动态",
  },

  components: {
    card
  },

  methods: {
 
  },

  created () {
    // let app = getApp()
  }
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
