<template>
  <v-app dark>
    <v-app-bar elevate-on-scroll fixed app color="light-blue darken-2">
      <v-app-bar-nav-icon to="/">
        <v-avatar>
          <img src="/icon.png" alt="favicon" />
        </v-avatar>
      </v-app-bar-nav-icon>

      <!-- <v-toolbar-title v-if="$vuetify.breakpoint.mdAndUp" v-text="title" /> -->
      <v-toolbar-title
        :class="{
          'subtitle-2': $vuetify.breakpoint.smAndDown
        }"
        v-text="title"
      />
      <v-spacer />

      <Navigation />
      <!-- <v-btn text class="text-none" nuxt to="/study">
        <v-icon left>mdi-library</v-icon>
        Study
      </v-btn>
      <v-btn text class="text-none" nuxt to="/sponsors">
        <v-icon left>mdi-hand-heart</v-icon>
        Sponsors
      </v-btn>
      <v-btn text class="text-none" nuxt to="/about">
        <v-icon left>mdi-information</v-icon>
        About
      </v-btn> -->
    </v-app-bar>
    <v-content>
      <nuxt />
    </v-content>

    <Footer />
  </v-app>
</template>

<script>
import Footer from '@/components/Footer.vue'
import Navigation from '@/components/Navigation.vue'
export default {
  components: {
    Footer,
    Navigation
  },
  data() {
    return {
      fixed: false,
      title: 'Covid-19 Educator'
    }
  }
}
</script>
