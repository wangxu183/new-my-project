<template>
  <div > 
        
            <view class="box head">乌江源上的秘密</view>
            <view class="first">
             <text decode="true" space="true">&nbsp;&nbsp;
             乌江源百里画廊旅游区属国家级旅游资源。\n</text>
            </view>
             <text>\n</text>

            <view class="text">
            <text  decode="true" space="true">&nbsp;&nbsp;
            位于黔西县南部，321国道公路旁，因修建东风水电站而形成。
            湖区总长62千米，宽度60-1000米之间，湖水面积近20平方千米。
            湖水清澄，倒影沉碧，宁静秀丽,两岸峰壁险峻，气势恢弘，且多瀑布山泉跌落湖中，
            是千里乌江上最美的崖壁画廊。景区交通方便，距省城贵阳80千米，距黔西城33千米，
            水路连通国家级风景名胜区织金洞，形成贵阳西部风光一绝。\n</text>
            <text>\n</text>
            </view>
          
            <img src="cloud://wangxu-44b924.7761-wangxu-44b924/images/timg.jpg" width="100%" height="200px">
            <view class="text">
              <text  decode="true" space="true">&nbsp;&nbsp;
              乌江是长江南岸最大的一级支流，全长1050公里,乌江有南、北两条河，南源三岔河发源于威宁县的香炉山，
              北源六冲河发源于赫章县的大坡山，两源在被国家文化部命名为“中国民间文化艺术之乡”、
              被中国村社发展会命名为“中国特色旅游村”的黔西县新仁乡化屋基汇合,化屋基以上至香炉山为乌江的上游段，
              以下至思南为乌江中游段，思南至涪陵入长江段为乌江下游段。\n</text>
              <text>\n</text>
             <text  decode="true" space="true">&nbsp;&nbsp; 
               从毕节地区威宁县的香炉山、
               赫章县的大坡山“两源”发源地至汇合处东风湖(化屋基)至荆江野济河，
              湖水清澈澄深，倒影沉碧，宁静秀丽，两岸峰壁险峻，气势恢宏，
              断层壁画神秘多姿，鬼斧神工，景观众多，有“山似三峡而水胜三峡，
              水似漓江而山胜漓江”的美誉，是千里乌江上最美的崖壁画廊，因此称乌江源百里画廊。\n</text>
              <text>\n</text>
              </view>
              

  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data : {
   
    },
  
   onLoad (option){
   console.log(option.type)
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
img{
  width:340px;
  height:150px;
  margin-top:15px;
  margin-bottom:15px;
  margin-left:15px;
}
.text{
  font-size:16px;
  font-weight:450;
  margin-left:10px;
  margin-right:10px;
}
.first{
  font-size:16px;
  font-weight:450;
  margin-left:10px;
  margin-right:10px;
  margin-top:30px;
}
.box{
  display:block;
  width:400px;
  height:40px;
  border-bottom:1px solid #EEE9E9;
  padding-top:10px;
}
.head{
  font-weight:650;
  margin-left:20px;
}
</style>
