<template>
  <div>
    <template v-if="$vuetify.breakpoint.mdAndUp">
      <v-btn text class="text-none" nuxt to="/" v-show="route !== '/'">
        <v-icon left>mdi-home</v-icon>
        Home
      </v-btn>
      <v-btn
        text
        class="text-none"
        nuxt
        to="/study"
        v-show="route !== '/study'"
      >
        <v-icon left>mdi-library</v-icon>
        Study
      </v-btn>
      <!-- <v-btn
        text
        class="text-none"
        nuxt
        to="/sponsors"
        v-show="route !== '/sponsors'"
      >
        <v-icon left>mdi-hand-heart</v-icon>
        Sponsors
      </v-btn> -->
      <v-btn
        text
        class="text-none"
        nuxt
        to="/about"
        v-show="route !== '/about'"
      >
        <v-icon left>mdi-information</v-icon>
        About
      </v-btn>
    </template>
    <v-menu v-else>
      <template v-slot:activator="{ on }">
        <v-btn icon v-on="on">
          <v-icon>mdi-format-list-bulleted-square</v-icon>
        </v-btn>
      </template>
      <v-card color="primary" dark>
        <v-list color="transparent">
          <v-list-item v-show="route !== '/'">
            <v-btn text class="text-none" nuxt to="/">
              <v-icon left>mdi-home</v-icon>
              Home
            </v-btn>
          </v-list-item>
          <v-list-item v-show="route !== '/study'">
            <v-btn text class="text-none" nuxt to="/study">
              <v-icon left>mdi-library</v-icon>
              Study
            </v-btn>
          </v-list-item>
          <!-- <v-list-item v-show="route !== '/sponsors'">
            <v-btn text class="text-none" nuxt to="/sponsors">
              <v-icon left>mdi-hand-heart</v-icon>
              Sponsors
            </v-btn>
          </v-list-item> -->
          <v-list-item v-show="route !== '/about'">
            <v-btn text class="text-none" nuxt to="/about">
              <v-icon left>mdi-information</v-icon>
              About
            </v-btn>
          </v-list-item>
        </v-list>
      </v-card>
    </v-menu>
  </div>
</template>

<script>
export default {
  computed: {
    route() {
      return this.$route.path
    }
  }
}
</script>

<style lang="scss" scoped></style>
