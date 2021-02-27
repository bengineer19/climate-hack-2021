<template>
  <v-container fluid id="main-cont">
    <v-layout row wrap>
      <v-row wrap>
        <v-col sm="12" md="4" lg="3">
          <ProfileCard :farmer="farmer" />
        </v-col>
        <v-col sm="12" md="8" lg="9">
          <ProjectList :projects="farmer.projects" />
        </v-col>
      </v-row>
    </v-layout>
  </v-container>
</template>

<script>
import ProfileCard from "~/components/ProfileCard.vue";
import ProjectList from "~/components/ProjectList.vue";

export default {
  components: {
    ProfileCard,
    ProjectList
  },
  data: () => ({
    farmer: {
      farmerName: "Markus Sudhoff",
      subtitle: "Member since Oct 2020",
      projects: [
        {
          name: "Agroforestry trial",
          started: "14/11/2020"
        }
      ]
    }
  })
};
</script>

<style scoped>
#main-cont {
  margin: 0;
}
</style>
