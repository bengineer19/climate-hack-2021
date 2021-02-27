<template>
  <!-- <v-card max-width="300" id="profile-card" color="amber darken-2" dark>
    <v-list-item-title class="headline">
      {{ project.name }}
    </v-list-item-title>
    <v-list-item-subtitle>{{ project.started }}</v-list-item-subtitle>
  </v-card> -->
  <v-stepper alt-labels>
    <v-card-title>{{ project.name }}</v-card-title>

    <v-card-text>
      Verification: 23rd April 2021
    </v-card-text>

    <v-stepper-header>
      <v-stepper-step step="1" complete>
        Applied
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="2" complete>
        Approved
      </v-stepper-step>

      <!-- <v-divider></v-divider>

      <v-stepper-step step="3" complete>
        Contract sent
      </v-stepper-step> -->

      <v-divider></v-divider>

      <v-stepper-step step="4">
        Contract received
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="5">
        Payment sent
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="6">
        Training received
      </v-stepper-step>
    </v-stepper-header>
  </v-stepper>
</template>

<script>
export default {
  props: ["project"]
};
</script>
