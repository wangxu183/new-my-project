<template>
  <div style="width: 100%; height:100%;">
 
      <map
        id="map"
        longitude="114.352085"
        latitude="30.595681"
        :scale="scale"
        :controls="controls"
        @controltap="controltap"
        :markers="markers"
        @markertap="markertap"
        :polyline="polyline"
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
      scale:14,
      markers: [{
      iconPath: '/static/images/marker.png',
      id: 0,
      latitude: 30.595681,
      longitude:114.352085,
      width: 50,
      height: 50
    }],
    polyline: [{
      points: [{
        longitude: 114.340713,
        latitude: 30.58292
      }, {
        longitude: 114.352085,
        latitude: 30.595681
      }],
      color: '#FF0000DD',
      width: 2,
      dottedLine: true
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
