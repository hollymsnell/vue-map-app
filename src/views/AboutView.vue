<template>
  <div class="about">
    <h1>This is a map</h1>
    <div id="map"></div>
  </div>
</template>

<script>
/* global mapboxgl */
export default {
  data: function () {
    return {};
  },
  mounted: function () {
    mapboxgl.accessToken = process.env.VUE_APP_MAP_API_KEY;
    const map = new mapboxgl.Map({
      container: "map", // container ID
      style: "mapbox://styles/mapbox/streets-v11", // style URL
      center: [-104.8214, 38.8339], // starting position [lng, lat]
      zoom: 9, // starting zoom
    });
    console.log(map);
  },
  methods: {},
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#map {
  width: 100%;
  height: 400px;
}
</style>
