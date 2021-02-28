<template>
  <v-app>
    <v-app-bar app flat :clipped-left="clipped">
      <!-- <v-app-bar :clipped-left="clipped" fixed app> -->
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <div class="d-flex align-center">
        <!-- <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        /> -->
        <!-- 
        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        /> -->
        <v-toolbar-title
          ><NuxtLink to="/" id="home-link">Syntropic</NuxtLink> | Farmer
          Area</v-toolbar-title
        >
      </div>

      <v-spacer></v-spacer>

      <!-- <v-btn href="https://github.com/" target="_blank" text>
        <span class="mr-2">Code</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn> -->
    </v-app-bar>
    <!-- <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main> -->
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <!-- <v-divider></v-divider> -->

      <!-- Exceptions -->
      <!-- <v-list>
        <v-list-item to="/apply">
          <v-list-item-action>
            <v-icon>mdi-pencil</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Apply</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list> -->

      <!-- <v-divider></v-divider>

      <v-list>
        <v-list-item to="/account">
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list> -->
    </v-navigation-drawer>

    <!-- <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" /> -->
    <!-- <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn> -->
    <!-- </v-app-bar> -->
    <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>

    <!-- <v-footer :absolute="!fixed" app>
      <span>&copy; Syntropic {{ new Date().getFullYear() }}</span>
    </v-footer> -->
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: true,
      drawer: true,
      fixed: false,
      items: [
        {
          icon: "mdi-view-dashboard",
          title: "Dashboard",
          to: "/farmer"
        },
        {
          icon: "mdi-account-group",
          title: "Communities",
          to: "/communities"
        },
        {
          icon: "mdi-check-bold",
          title: "Offset verification",
          to: "/verification"
        },
        {
          icon: "mdi-view-list",
          title: "My projects",
          to: "/projects"
        }
        // {
        //   icon: "mdi-apps",
        //   title: "Apply",
        //   to: "/communities",
        //   divider: true
        // },
        // {
        //   icon: "mdi-chart-bubble",
        //   title: "Account",
        //   to: "/account"
        // }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  },
  head: {
    title: "Farmer area"
  }
};
</script>

<style scoped>
#home-link {
  text-decoration: none;
  color: inherit;
}
.v-application {
  /* background-color: #f5f5f5; */
}
</style>
