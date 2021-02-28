<template>
  <v-card max-width="300" id="profile-card" :color="farmer.color" dark>
    <v-list-item-content class="justify-center">
      <div class="mx-auto text-center">
        <v-avatar size="150" class="rounded-circle text-center">
          <img :src="require('../assets/' + farmer.photo + '.png')" />
        </v-avatar>
      </div>
    </v-list-item-content>

    <v-list-item-title class="headline">
      {{ farmer.farmerName }}
    </v-list-item-title>
    <v-list-item-subtitle>{{ farmer.subtitle }}</v-list-item-subtitle>

    <v-card-text>
      <div class="profile-text">
        <div>
          <strong>Projects:</strong>
          {{ farmer.projects.new.concat(farmer.projects.ongoing).length }}
        </div>
      </div>
      <div class="profile-text">
        <div><strong>Tel no:</strong> {{ farmer.tel }}</div>
      </div>
    </v-card-text>

    <div id="map-wrap" style="height: 20vh">
      <client-only>
        <!-- <l-map :zoom="13" :center="[55.9464418, 8.1277591]"> -->
        <l-map :zoom="13" :center="[farmer.coord.lat, farmer.coord.long]">
          <l-tile-layer
            url="http://{s}.tile.osm.org/{z}/{x}/{y}.png"
          ></l-tile-layer>
          <l-marker :lat-lng="[farmer.coord.lat, farmer.coord.long]"></l-marker>
        </l-map>
      </client-only>
    </div>
  </v-card>
</template>

<script>
export default {
  props: ["farmer"]
};
</script>

<style scoped>
#profile-card {
  padding: 20px;
  margin: 0 auto;
}

.profile-text {
  color: white;
  font-size: 1.1em;
  padding-bottom: 10px;
}
</style>
