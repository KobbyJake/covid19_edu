<template>
  <v-layout class="wall" fill-height>
    <v-container fill-height>
      <v-row d-flex wrap align="center">
        <v-col md="7" cols="12">
          <p
            :class="{
              headline: $vuetify.breakpoint.smAndDown,
              'display-3': $vuetify.breakpoint.mdAndUp,
              'font-weight-black': true
            }"
          >
            COVID-19 Educator.
          </p>
          <hr />
          <br />
          <p
            :class="{
              'subtitle-2': $vuetify.breakpoint.smAndDown,
              headline: $vuetify.breakpoint.mdAndUp,
              'font-weight-light': true
            }"
          >
            Get to know about this disease. Understand the myths and facts,
            safety precautions to prevent COVID-19 infection and also manage
            infection.
          </p>
          <br />
          <v-btn outlined rounded large class="text-none" nuxt to="/study"
            ><v-icon left>mdi-library</v-icon>Start learning</v-btn
          >
        </v-col>
        <v-col class="animated fadeInLeftBig" md="5" cols="12">
          <v-container text-center align-center justify-center>
            <!-- <p>{{ stats }}</p> -->
            <!-- <v-playback
              ref="covidrun"
              url="/covidrun.mp4"
              auto-play="play"
            ></v-playback> -->
            <img
              v-if="!ready"
              src="~assets/medicare.svg"
              alt="medical care"
              width="400vw"
            />
            <v-card
              v-if="ready"
              class="mx-auto"
              max-width="400"
              elevation="24"
              color="indigo darken-4"
            >
              <!-- <img
                src="~assets/medicare.svg"
                alt="medical care"
                width="150vw"
              /> -->

              <v-list-item two-line>
                <v-list-item-content>
                  <v-list-item-title class="headline"
                    >Latest Update in Ghana</v-list-item-title
                  >
                  <v-list-item-subtitle
                    >{{ stats.ghana.date }}
                    {{ stats.ghana.time }}</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
              <v-avatar :size="90">
                <img src="/icon.png" alt="favicon" />
              </v-avatar>
              <v-list class="transparent">
                <v-list-item>
                  <v-list-item-title>Confirmed Cases</v-list-item-title>

                  <v-list-item-icon>
                    <v-icon color="yellow">mdi-account-group</v-icon>
                  </v-list-item-icon>

                  <v-list-item-subtitle
                    class="text-right font-weight-black headline"
                  >
                    {{ stats.ghana.confirmed }}
                  </v-list-item-subtitle>
                </v-list-item>
                <v-list-item>
                  <v-list-item-title>Recovered Cases</v-list-item-title>

                  <v-list-item-icon>
                    <v-icon color="green">mdi-run-fast</v-icon>
                  </v-list-item-icon>

                  <v-list-item-subtitle
                    class="text-right font-weight-black headline"
                  >
                    {{ stats.ghana.recovered }}
                  </v-list-item-subtitle>
                </v-list-item>
                <v-list-item>
                  <v-list-item-title>Deaths Recorded</v-list-item-title>

                  <v-list-item-icon>
                    <v-icon color="red">mdi-account-multiple-remove</v-icon>
                  </v-list-item-icon>

                  <v-list-item-subtitle
                    class="text-right font-weight-black headline"
                  >
                    {{ stats.ghana.deaths }}
                  </v-list-item-subtitle>
                </v-list-item>
              </v-list>

              <v-divider></v-divider>

              <v-card-actions>
                <v-btn-toggle :dense="true" rounded>
                  <v-btn
                    text
                    class="text-none"
                    href="https://www.ghanahealthservice.org/covid19/"
                    target="_blank"
                    rel="noopener noreferrer"
                    >Ghana Health Service</v-btn
                  >
                  <v-btn
                    text
                    class="text-none"
                    href="https://www.who.int/westernpacific/emergencies/covid-19/news-covid-19"
                    target="_blank"
                    rel="noopener noreferrer"
                    >W.H.O.</v-btn
                  >

                  <v-btn
                    text
                    class="text-none"
                    href="https://www.coronatracker.com/"
                    target="_blank"
                    rel="noopener noreferrer"
                    >Corona Tracker</v-btn
                  >
                </v-btn-toggle>
              </v-card-actions>
            </v-card>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      ready: false,
      stats: {}
    }
  },
  methods: {
    registerStudent() {
      this.student.user_name =
        this.student.first_name.charAt(0) + this.student.last_name
      this.student.user_name =
        this.student.class_of_study + this.student.region_of_school
      // await prisma.student.create({
      //   data: this.student
      // })
    },
    submit() {
      if (this.$refs.form.validate()) {
        // Native form submission is not yet supported
        // axios.post('/api/submit', {
        //   name: this.name,
        //   email: this.email,
        //   select: this.select,
        //   checkbox: this.checkbox
        // })
        this.$toast.success('Registraton complete', {
          iconPack: 'mdi',
          icon: 'mdi-content-save'
        })
        this.$router.push('/study')
      }
    },
    clear() {
      this.$refs.form.reset()
    }
  },
  mounted() {
    this.$axios.get('https://mazitekgh.com/covid19/v1/').then((res) => {
      this.stats = res.data
      this.ready = true
    })
  }
}
</script>
<style>
.wall {
  background: url(~assets/cool-background.png) no-repeat center fixed;
  background-size: cover;
}
</style>
