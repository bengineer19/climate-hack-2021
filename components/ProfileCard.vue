<template>
  <v-card max-width="300" id="profile-card" color="amber darken-2" dark>
    <v-list-item-content class="justify-center">
      <div class="mx-auto text-center">
        <v-avatar size="150" class="rounded-circle text-center">
          <img src="~assets/alexandre.png" />
        </v-avatar>
      </div>
    </v-list-item-content>

    <v-list-item-title class="headline">
      {{ farmer.farmerName }}
    </v-list-item-title>
    <v-list-item-subtitle>{{ farmer.subtitle }}</v-list-item-subtitle>

    <v-card-text>
      <div class="profile-text">
        <div>Projects: {{ farmer.projects.length }}</div>
      </div>
    </v-card-text>

    <div id="map-wrap" style="height: 20vh">
      <client-only>
        <!-- <l-map :zoom="13" :center="[55.9464418, 8.1277591]"> -->
        <l-map :zoom="13" :center="[-23.121037, -46.196555]">
          <l-tile-layer
            url="http://{s}.tile.osm.org/{z}/{x}/{y}.png"
          ></l-tile-layer>
          <l-marker :lat-lng="[-23.121037, -46.196555]"></l-marker>
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
}
</style>
