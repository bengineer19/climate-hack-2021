<template>
  <!-- <v-card max-width="300" id="profile-card" color="amber darken-2" dark>
    <v-list-item-title class="headline">
      {{ project.name }}
    </v-list-item-title>
    <v-list-item-subtitle>{{ project.started }}</v-list-item-subtitle>
  </v-card> -->
  <v-stepper alt-labels>
    <v-card-title>{{ project.name }}</v-card-title>
    <v-card-subtitle>Started {{ project.started }}</v-card-subtitle>

    <v-card-text>
      <v-alert text v-if="project.verification" type="info">
        Upcoming CO2 verification: {{ project.verification }}
      </v-alert>
    </v-card-text>

    <v-stepper-header>
      <v-stepper-step step="1" :complete="project.completed >= 1">
        Applied
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="2" :complete="project.completed >= 2">
        Approved
      </v-stepper-step>

      <!-- <v-divider></v-divider>

      <v-stepper-step step="3" complete>
        Contract sent
      </v-stepper-step> -->

      <v-divider></v-divider>

      <v-stepper-step step="3" :complete="project.completed >= 3">
        Contract received
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="4" :complete="project.completed >= 4">
        Payment sent
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="5" :complete="project.completed >= 5">
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
