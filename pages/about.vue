<template>
  <v-layout class="wall" fill-height>
    <v-container text-center align-center justify-center>
      <v-row align="center" justify="center">
        <v-col cols="10" sm="8" lg="6">
          <v-card
            class="mx-auto animate__animated animate__backInUp"
            max-width="500"
            elevation="24"
            color="indigo darken-4"
          >
            <v-list-item two-line>
              <v-list-item-content>
                <v-list-item-title class="headline font-weight-black"
                  >About Covid-19 Educator
                </v-list-item-title>
                <v-list-item-subtitle
                  >Covid-19 Education for all</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
            <v-avatar :size="$vuetify.breakpoint.mdAndUp ? 100 : 60">
              <img src="/icon.png" alt="favicon" />
            </v-avatar>
            <br />
            <v-divider></v-divider>
            <h3 class="text-left mx-4 font-weight-medium">
              Education is key in the battle against this pandemic. This
              application has been developed to educate our final year students
              across the nation as they get back to school.
            </h3>
            <!-- <p>
              This application is temporarily hosted. I am by this means
              appealing for your financial support (as a sponsor) to host this
              application on a permanent domain and to mantain it for as long as
              it will be relevant.
            </p>
            <p>
              Your kind gesture will not go unnoticed as your profile will be
              featured prominently on the sponsors page for all to know and
              appreciate your contribution to a worthy course. Thank you.
            </p> -->
            <br />
            <v-divider></v-divider>
            <v-card-actions>
              <v-row align="center" justify="center">
                <p>
                  I am Jake Appiah Baah, ICT tutor at J.E. Atta-Mills SHS The
                  developer of Educov App. Contact: 0242525727 email:
                  appiahbaahjake@gmail.com
                </p>
              </v-row>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
