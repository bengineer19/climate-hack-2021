<template>
  <div>
    <v-container>
      <div class="text-h2">CO2 sequestration verification</div>
      <br />
      <div class="text-h4">Upcoming site visits</div>
      <VerificationCard :verification="verification" />
      <div class="text-h4">Past site visits</div>
      <VerificationCard :verification="verification2" />
    </v-container>
  </div>
</template>

<script>
import VerificationCard from "~/components/VerificationCard.vue";

// import dummyFarmer from "~/dummyData.js";

export default {
  layout: "farmerLayout",
  components: {
    VerificationCard
  },
  data: () => ({
    verification: {
      date: "4th March 2021",
      location: "Tatu",
      verifier: "Ricardo Queiroz Linhares"
    },
    verification2: {
      date: "1st May 2020",
      location: "Matinha",
      verifier: "Danilo Assis Caetano",
      past: true
    }
  })
};
</script>
