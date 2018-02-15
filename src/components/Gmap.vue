<template>
  <div class="google-map" :id="mapName"></div>
</template>
<script>
export default {
  name: 'google-map',
  props: ['name'],
  data: function () {
    return {
      mapName: this.name + "-map",
      markerCoordinates: [{
        latitude: -6.284720,
        longitude: 107.170710
      }],
      map: null,
      bounds: null,
      markers: []
    }
  },
  mounted: function () {
    this.bounds = new google.maps.LatLngBounds();
    const element = document.getElementById(this.mapName)
    const mapCentre = this.markerCoordinates[0]
    const map_zoom = 16
    const style = [{
      "stylers": [{
        "hue": "#03a9f4"
      }, {
        "saturation": 10
      }, {
        "gamma": 2.15
      }, {
        "lightness": 12
      }]
    }];
    const options = {
      center: new google.maps.LatLng(mapCentre.latitude, mapCentre.longitude),
      zoom: map_zoom,
      panControl: true,
      zoomControl: true,
      mapTypeControl: true,
      streetViewControl: true,
      mapTypeId: google.maps.MapTypeId.ROADMAP,
      scrollwheel: false,
      styles: style
    }
    this.map = new google.maps.Map(element, options);
    this.markerCoordinates.forEach((coord) => {
      const position = new google.maps.LatLng(coord.latitude, coord.longitude);
      const marker = new google.maps.Marker({
        position,
        map: this.map,
        visible: true,
        icon: 'https://pusc.or.id/assets/img/pin.png'
      });
      const contentString = '<div id="mapcontent">' + '<p>President University Campus Jalan Ki Hajar Dewantara, Jababeka Education Park Cikarang, West Java 17550</p></div>';
      const infowindow = new google.maps.InfoWindow({
        maxWidth: 320,
        content: contentString
      });

      google.maps.event.addListener(marker, 'click', function() {
        infowindow.open(this.map, marker);
      });
    });
  }
};
</script>
<style scoped>
</style>
