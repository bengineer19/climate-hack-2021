<template>
  <div>
    <v-container fluid id="main-cont">
      <v-layout row wrap>
        <v-row wrap>
          <v-col sm="12" md="4" lg="3">
            <ProfileCard :farmer="farmer" />
          </v-col>
          <v-col sm="12" md="8" lg="9">
            <ProjectList
              :projects="farmer.projects.new.concat(farmer.projects.ongoing)"
            />
          </v-col>
        </v-row>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import ProfileCard from "~/components/ProfileCard.vue";
import ProjectList from "~/components/ProjectList.vue";

import dummyFarmer from "~/dummyData.js";

export default {
  layout: "farmerLayout",
  components: {
    ProfileCard,
    ProjectList
  },
  data: () => ({
    farmer: dummyFarmer
  })
};
</script>

<style scoped>
#main-cont {
  margin: 0;
}
</style>
