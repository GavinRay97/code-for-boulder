<template>
  <googlemaps-map
   id="map"
   :center="{
     lat: 40.0150,
     lng: -105.2705
    }"
    :zoom="13">
</googlemaps-map>
</template>

<script>
export default {
  name: "MapCard"
}
</script>

<style>
  #map {
    position: initial;
  }
</style>
