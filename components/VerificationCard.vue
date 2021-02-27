<template>
  <v-card class="verif-card" max-width="600" color="blue" dark>
    <v-card-title class="headline">
      {{ verification.date }}
    </v-card-title>

    <v-card-subtitle>
      You {{ verification.past ? "were" : "will be" }} visited by
      {{ verification.verifier }} at your agroforestry project in
      {{ verification.location }}.
    </v-card-subtitle>

    <v-card-subtitle v-if="!verification.past">
      Further details will be sent via text message</v-card-subtitle
    >

    <v-card-actions v-if="!verification.past">
      <v-btn text>
        Reschedule
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: ["verification"]
};
</script>

<style scoped>
.verif-card {
  margin: 20px 0;
}
</style>
