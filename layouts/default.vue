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
      <v-btn text class="text-none" nuxt to="/login">
        <v-icon>mdi-lock-open</v-icon>
        login
      </v-btn>
    </v-app-bar>
    <v-content>
      <nuxt />
    </v-content>

    <v-footer :fixed="fixed" app color="light-blue darken-2">
      <span>Project &copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      // clipped: false,
      // drawer: false,
      fixed: false,
      title: 'Covid-19 Educator'
    }
  }
}
</script>
