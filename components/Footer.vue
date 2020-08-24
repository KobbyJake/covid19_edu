<template>
  <v-footer fixed app color="light-blue darken-2">
    <v-row justify="center">
      <span
        :class="{
          'subtitle-2': $vuetify.breakpoint.smAndDown
        }"
        >By Jake Appiah Baah
      </span>
      <v-divider class="mx-4" vertical></v-divider>
      <a href="mailto:appiahbaahjake@gmail.com"><v-icon>mdi-gmail</v-icon></a>

      <v-divider class="mx-4" vertical></v-divider>
      <a href="http://twitter.com/@kobbyjake_" target="_blank"
        ><v-icon>mdi-twitter</v-icon></a
      >

      <v-divider class="mx-4" vertical></v-divider>

      <a href="https://github.com/KobbyJake" target="_blank"
        ><v-icon>mdi-github</v-icon></a
      >
      <v-divider class="mx-4" vertical></v-divider>
    </v-row>
  </v-footer>
  <!-- <v-footer fixed app color="light-blue darken-2">
    <v-row justify="center">
      <span
        :class="{
          'subtitle-2': $vuetify.breakpoint.smAndDown
        }"
        >Be safe &copy;{{ new Date().getFullYear() }}
      </span>
    </v-row>
  </v-footer> -->
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
