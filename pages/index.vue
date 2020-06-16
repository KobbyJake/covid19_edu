<template>
  <v-layout class="wall" fill-height>
    <v-container fill-height>
      <v-row d-flex wrap align="center">
        <v-col md="7" cols="12" class="animate__animated animate__fadeIn">
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
            Get to know more about this disease. Understand the myths and facts,
            safety precautions to prevent COVID-19 infection and how to manage
            infection.
          </p>
          <!-- <br /> -->
          <v-row>
            <div>
              <br />
              <br />
              <v-btn outlined rounded large class="text-none" nuxt to="/study"
                ><v-icon left>mdi-library</v-icon>Start learning</v-btn
              >
            </div>
            <!-- <v-divider vertical></v-divider> -->
            <v-spacer></v-spacer>
            <v-item-group>
              <v-subheader>Share &#10084;</v-subheader>
              <v-item>
                <vue-goodshare-facebook
                  button_design="outline"
                  page_url="https://educov.netlify.app"
                  has_icon
                ></vue-goodshare-facebook>
              </v-item>
              <v-item>
                <vue-goodshare-twitter
                  button_design="outline"
                  page_url="https://educov.netlify.app"
                  has_icon
                ></vue-goodshare-twitter>
              </v-item>
              <v-item>
                <vue-goodshare-whats-app
                  button_design="outline"
                  page_url="https://educov.netlify.app"
                  has_icon
                ></vue-goodshare-whats-app>
              </v-item>
            </v-item-group>
          </v-row>
        </v-col>
        <v-col class="animated fadeInLeftBig" md="5" cols="12">
          <v-container text-center align-center justify-center>
            <img
              v-if="!ready"
              class="mx-auto animate__animated animate__zoomIn"
              src="~assets/medicare.svg"
              alt="medical care"
              :width="$vuetify.breakpoint.mdAndUp ? 500 : 300"
            />
            <v-card
              v-if="ready"
              class="mx-auto animate__animated animate__backInUp"
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
                    >COVID-19 Cases
                  </v-list-item-title>
                  <v-list-item-subtitle
                    >{{ stats.ghana.date }}
                    {{ stats.ghana.time }}</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
              <v-avatar :size="$vuetify.breakpoint.mdAndUp ? 80 : 30">
                <img src="/icon.png" alt="favicon" />
              </v-avatar>

              <v-tabs background-color="indigo darken-4">
                <v-tab>🇬🇭 Ghana</v-tab>
                <v-tab>&#127759; Global</v-tab>
                <v-tab-item background-color="indigo darken-4">
                  <v-list class="transparent">
                    <v-list-item>
                      <v-list-item-title>Confirmed </v-list-item-title>

                      <v-list-item-icon>
                        <v-icon color="yellow" size="32"
                          >mdi-account-group</v-icon
                        >
                      </v-list-item-icon>

                      <v-list-item-subtitle
                        class="text-right font-weight-black headline"
                      >
                        {{ stats.ghana.confirmed }}
                      </v-list-item-subtitle>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-title>Recoveries</v-list-item-title>

                      <v-list-item-icon>
                        <v-icon color="green" size="32">mdi-run-fast</v-icon>
                      </v-list-item-icon>

                      <v-list-item-subtitle
                        class="text-right font-weight-black headline"
                      >
                        {{ stats.ghana.recovered }}
                      </v-list-item-subtitle>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-title>Deaths</v-list-item-title>

                      <v-list-item-icon>
                        <v-icon color="red" size="32"
                          >mdi-account-multiple-remove</v-icon
                        >
                      </v-list-item-icon>

                      <v-list-item-subtitle
                        class="text-right font-weight-black headline"
                      >
                        {{ stats.ghana.deaths }}
                      </v-list-item-subtitle>
                    </v-list-item>
                  </v-list>
                </v-tab-item>
                <v-tab-item background-color="indigo darken-4">
                  <v-list class="transparent">
                    <v-list-item>
                      <v-list-item-title>Confirmed </v-list-item-title>

                      <v-list-item-icon>
                        <v-icon color="yellow" size="32"
                          >mdi-account-group</v-icon
                        >
                      </v-list-item-icon>

                      <v-list-item-subtitle
                        class="text-right font-weight-black headline"
                      >
                        {{ stats.global.confirmed }}
                      </v-list-item-subtitle>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-title>Recoveries </v-list-item-title>

                      <v-list-item-icon>
                        <v-icon color="green" size="32">mdi-run-fast</v-icon>
                      </v-list-item-icon>

                      <v-list-item-subtitle
                        class="text-right font-weight-black headline"
                      >
                        {{ stats.global.recovered }}
                      </v-list-item-subtitle>
                    </v-list-item>
                    <v-list-item>
                      <v-list-item-title>Deaths </v-list-item-title>

                      <v-list-item-icon>
                        <v-icon color="red" size="32"
                          >mdi-account-multiple-remove</v-icon
                        >
                      </v-list-item-icon>

                      <v-list-item-subtitle
                        class="text-right font-weight-black headline"
                      >
                        {{ stats.global.deaths }}
                      </v-list-item-subtitle>
                    </v-list-item>
                  </v-list>
                </v-tab-item>
              </v-tabs>

              <v-divider></v-divider>

              <v-card-actions>
                <v-row align="center" justify="center">
                  <v-col cols="12">
                    Sources:
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

                      <!-- <v-btn
                    text
                    class="text-none"
                    href="https://www.coronatracker.com/"
                    target="_blank"
                    rel="noopener noreferrer"
                    >Corona Tracker</v-btn
                  > -->
                    </v-btn-toggle>
                  </v-col>
                </v-row>
              </v-card-actions>
            </v-card>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
// Import vue-goodshare single elements
import VueGoodshareFacebook from 'vue-goodshare/src/providers/Facebook.vue'
import VueGoodshareTwitter from 'vue-goodshare/src/providers/Twitter.vue'
import VueGoodshareWhatsApp from 'vue-goodshare/src/providers/WhatsApp.vue'
export default {
  name: 'Index Page',
  components: {
    VueGoodshareWhatsApp,
    VueGoodshareTwitter,
    VueGoodshareFacebook
  },
  data() {
    return {
      ready: false,
      stats: {}
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
