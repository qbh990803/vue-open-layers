<template>
  <div class="home">
    <div id="map" class="map-home"></div>
  </div>
</template>

<script setup name="OpenLayerMap">
import { onMounted, ref } from "vue";
import { Map, View } from "ol";
import * as olProj from "ol/proj";
import TileLayer from "ol/layer/Tile";
import XYZ from "ol/source/XYZ";
// import { Vector as VectorLayer} from 'ol/layer';
// import { Vector as VectorSource} from 'ol/source';

const openMap = ref();

function initMap() {
  openMap.value = new Map({
    target: "map",
    layers: [
      new TileLayer({
        source: new XYZ({
          url: "https://wprd0{1-4}.is.autonavi.com/appmaptile?lang=zh_cn&size=1&style=7&x={x}&y={y}&z={z}",
        }),
      }),
    ],
    view: new View({
      // 将西安作为地图中心
      center: olProj.fromLonLat([108.945951, 34.465262]),
      zoom: 1,
    }),
    controls: [],
  });
}

onMounted(() => {
  initMap();
});
</script>

<style scoped>
.map-home {
  width: 100vw;
  height: 100vh;
}
</style>
