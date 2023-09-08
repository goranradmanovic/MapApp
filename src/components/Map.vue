<script setup>
  import { MapboxMap, MapboxMarker, MapboxGeocoder, MapboxNavigationControl, MapboxGeolocateControl } from '@studiometa/vue-mapbox-gl'
  import 'mapbox-gl/dist/mapbox-gl.css'
  import '@mapbox/mapbox-gl-geocoder/lib/mapbox-gl-geocoder.css';

  const mapApiKey = import.meta.env.VITE_MAP_BOX_API_KEY
</script>

<template>
  <MapboxMap
    :access-token="mapApiKey"
    map-style="mapbox://styles/mapbox/streets-v11">
    <MapboxGeolocateControl />
    <MapboxGeocoder />
    <MapboxNavigationControl position="bottom-right" />
  </MapboxMap>
</template>