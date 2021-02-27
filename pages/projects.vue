<template>
  <div>
    <v-container>
      <ProjectList :projects="farmer.projects.new" title="New Projects" />
      <ProjectList
        :projects="farmer.projects.ongoing"
        title="Ongoing Projects"
      />
    </v-container>
  </div>
</template>

<script>
import ProjectList from "~/components/ProjectList.vue";

import dummyFarmer from "~/dummyData.js";

export default {
  layout: "farmerLayout",
  components: {
    ProjectList
  },
  data: () => ({
    farmer: dummyFarmer
  })
};
</script>
