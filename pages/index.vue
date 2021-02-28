<template>
  <v-container id="main-cont">
    <div class="text-center">
      <div class="text-h1">Syntropic</div>
      <div class="text-subtitle-1" id="intro">
        Syntropic uses the rapidly growing CO2 offset market to fund
        Agroforestry in Brazil. Low-income farmers now have a way to access the
        upfront capital and knowledge they need to convert their land to more
        productive agricultural practices.
      </div>
      <div class="text-subtitle-1" id="intro">
        In the process of lifting communities out of poverty, CO2 is
        sequestered. Farmers are incentivised to let trees to last for
        generations due to the food and sustainable income produced by
        agroforestry. This means the CO2 offsets produced are uniquely high
        quality.
      </div>

      <v-card
        class="mx-auto"
        max-width="800"
        color="light-blue lighten-3"
        shaped
      >
        <v-card-title>About our founder</v-card-title>

        <v-container>
          <v-row id="about-row">
            <v-col sm="12" lg="3">
              <v-avatar size="120" class="rounded-circle text-center">
                <img :src="require('../assets/alexandre.png')" />
              </v-avatar>
            </v-col>
            <v-col>
              <v-card-text>
                <div class="text-body-1">
                  Alexandre is the son of 4 generations of Brazilian farmers.
                  Seeing the unsustainable agriculture practices, poverty of
                  farmers, and unused potential for CO2 sequestration inspired
                  him to start Syntropic. He is intimately familiar with
                  agroforestry and the needs of Brazilian farmers.
                </div>
              </v-card-text>
            </v-col>
          </v-row>
        </v-container>
      </v-card>

      <br />

      <v-card
        class="mx-auto"
        max-width="800"
        color="light-blue lighten-3"
        shaped
      >
        <v-card-title>Our approach</v-card-title>

        <v-container>
          <v-row id="about-row">
            <v-col>
              <v-card-text>
                <div class="text-body-1">
                  We know that hands-on education by agroforestry ambassadors is
                  the best way to teach farmers syntropic agriculture practices
                  (e-learning is not feasible due to cultural and technological
                  constraints). We understand the process well, and are in
                  contact with over 40 agroforestry trainers in Brazil.
                </div>
              </v-card-text>
            </v-col>
            <v-col sm="12" lg="3">
              <v-avatar size="120" class="text-center">
                <img :src="require('../assets/teaching.jpeg')" />
              </v-avatar>
            </v-col>
          </v-row>
        </v-container>
      </v-card>

      <div class="text-h3 pt-4">Demo</div>

      <div>
        Click below to access our hackathon demo as a farmer. Please explore the
        platform by clicking on different pages.
      </div>
      <br />
      <v-btn to="/farmer" color="amber darken-2" class="white--text" nuxt>
        Login as farmer
      </v-btn>
    </div>
  </v-container>
</template>

<script>
export default {
  head: {
    title: "Home"
  }
};
</script>

<style scoped>
#intro {
  font-size: 1.3rem !important;
  max-width: 700px;
  margin: 20px auto;
}
#about-row {
  margin-bottom: 10px;
}
</style>
