<template>
  <div style="width: 100%; height:100%;">
 
      <map
        id="map"
        longitude="106.62304"
        latitude="26.67856"
        :scale="scale"
        :controls="controls"
        @controltap="controltap"
        :markers="markers"
        @markertap="markertap"
        @regionchange="regionchange"
        show-location
        style="width: 100%; height:100%;"
      ></map>
  </div>
</template>

<script>


export default {


  data () {
    return {
      scale:8,
      markers: [{
      iconPath: '/static/images/marker.png',
      id: 0,
      latitude: 26.67856,
      longitude:106.62304,
      width: 50,
      height: 50
    }],
    controls: [{
      id: 1,
      iconPath: '/static/images/dingwei.png',
      position: {
        left: 0,
        top: 300 - 50,
        width: 50,
        height: 50
      },
      clickable: true
    }]
    }
  },
    regionchange(e) {
    console.log(e.type)
  },
  markertap(e) {
    console.log(e.markerId)
  },
  controltap(e) {
    console.log(e.controlId)
  },

  created () {
  }
}
</script>

<style>
body,html{height:100%}

</style>
