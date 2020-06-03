<template>
  <v-app dark>
    <v-app-bar elevate-on-scroll fixed app color="light-blue darken-2">
      <v-app-bar-nav-icon to="/">
        <v-avatar>
          <img src="/icon.png" alt="favicon" />
        </v-avatar>
      </v-app-bar-nav-icon>

      <v-toolbar-title v-text="title" />
      <v-spacer />

      <v-btn text class="text-none" nuxt to="/study">
        <v-icon>mdi-library</v-icon>
        study
      </v-btn>
    </v-app-bar>
    <v-content>
      <nuxt />
    </v-content>

    <v-footer :fixed="fixed" app color="light-blue darken-2">
      <v-row justify="center">
        <span>Made by Jake Appiah Baah </span>
        <v-divider class="mx-4" vertical></v-divider>
        <a href="mailto:appiahbaahjake@gmail.com"><v-icon>mdi-gmail</v-icon></a>

        <v-divider class="mx-4" vertical></v-divider>
        <a href="http://twitter.com/@kobbyjake_" target="_blank"
          ><v-icon>mdi-twitter</v-icon></a
        >

        <v-divider class="mx-4" vertical></v-divider>
        <!-- <a
          href="http://facebook.com/appiahbaahjake"
          target="_blank"
          rel="noopener noreferrer"
          ><v-icon>mdi-facebook</v-icon></a
        > -->
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      fixed: false,
      title: 'Covid-19 Educator'
    }
  }
}
</script>
