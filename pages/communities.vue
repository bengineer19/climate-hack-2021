<template>
  <div>
    <v-container fluid id="main-cont">
      <v-layout row wrap>
        <v-row wrap>
          <v-col
            sm="12"
            md="4"
            lg="3"
            xl="2"
            v-for="farmer in community"
            :key="farmer.tel"
          >
            <ProfileCard :farmer="farmer" />
          </v-col>
        </v-row>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import ProfileCard from "~/components/ProfileCard.vue";

import { community } from "~/dummyData.js";

export default {
  layout: "farmerLayout",
  components: {
    ProfileCard
  },
  data: () => ({
    community: community
  })
};
</script>

<style scoped>
#main-cont {
  margin: 0;
}
</style>
