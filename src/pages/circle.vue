<template>
  <div class="container">
    <navbar title="设置圆形"></navbar>
    <weex-amap class="map" id="map2017" geolocation="true" :sdk-key="keys" :zoom="zoom" :center="pos">
      <weex-amap-circle :center="pos" radius="7000" fill-color="#2ecc71" fill-width="4"></weex-amap-circle>
    </weex-amap>
    <div class="map-control">
      <text class="title">Componenet: weex-amap-circle</text> 
      <text class="tips">可以在地图上绘制圆形</text>
    </div>
  </div>
</template>

<style>
  .container{
    position: relative;
    flex:1; 
    background-color: #fff;
  }
  .map{
    flex: 1;
    position: relative;
    background-color: #fff;
    min-height: 800;
    border-bottom-width: 10;
    border-bottom-color: #fff;
  }
  .map-control{
    padding-top: 20;
    min-height: 600;
  }
  .title{
    margin-left: 20;
    padding-left: 20;
    padding-top: 10;
    padding-bottom: 10;
    font-size: 36px;
    border-left-width: 6;
    border-left-color: #0f89f5;
    color: #222;
    text-align: left;
  }
  .tips{
    margin: 20;
    padding: 10;
    color:#666;
    font-size: 20px;
  }
</style>

<script>
  import Navbar from '../include/navbar.vue'
  var Amap = null;
  try {
    Amap = weex.requireModule('amap');
  } catch(err) {
    console.log(err);
  }
  export default {
      components: {Navbar},
      data() {
          return {
              keys: {
                  h5: 'f4b99dcd51752142ec0f1bdcb9a8ec02',
                  ios: '',
                  android: 'db6a973159cb0c2639ad02c617a786ae'
              },
              pos: [116.397428, 39.90923],
              zoom: 9
          }
      }
  }
</script>