<template>
  <v-app dark>
    <v-app-bar elevate-on-scroll fixed app color="light-blue darken-2">
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
    <!-- <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
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
