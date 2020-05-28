<template>
  <v-layout class="wall" fill-height>
    <v-container fill-height>
      <v-row d-flex reverse wrap>
        <v-col>
          <p class="font-weight-black display-3 animated fadeInRightBig">
            COVID-19 Educator.
          </p>
          <p class="font-weight-medium display-1 animated fadeInRightBig">
            Students' login
          </p>
          <hr />
          <!-- <br /> -->
          <v-container grid-list-xs>
            <v-card shaped raised max-width="500px">
              <!-- <v-divider></v-divider> -->
              <v-card-text>
                <v-form ref="form" v-model="valid" lazy-validation>
                  <v-text-field
                    ref="username"
                    v-model="email"
                    label="User name"
                    :rules="userNameRules"
                    prepend-inner-icon="mdi-account"
                  ></v-text-field>
                  <v-text-field
                    v-if="mode == 'login' || mode == 'register'"
                    ref="password"
                    v-model="password"
                    label="Password"
                    hint="At least 8 characters"
                    min="8"
                    :rules="pswdRules"
                    :counter="8"
                    prepend-inner-icon="mdi-lock"
                    :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                    :type="showPassword ? 'text' : 'password'"
                    @click:append="showPassword = !showPassword"
                  ></v-text-field>
                </v-form>
              </v-card-text>
              <!-- <v-divider></v-divider> -->
              <v-card-actions>
                <v-tooltip top>
                  <template v-slot:activator="{ on }">
                    <v-btn fab dark small v-on="on" @click="clear"
                      ><v-icon>mdi-backspace</v-icon>
                    </v-btn>
                  </template>
                  <span>Clear inputs</span>
                </v-tooltip>
                <v-spacer></v-spacer>
                <v-btn
                  outlined
                  rounded
                  color="default"
                  class="text-none"
                  @click="submit"
                  >Submit</v-btn
                >
              </v-card-actions>
            </v-card>
          </v-container>
          <br />
        </v-col>
        <v-col class="animated fadeInLeftBig">
          <v-container text-center align-center justify-center>
            <img src="~assets/login.svg" alt="shsc logo" width="400vw" />
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>
<script>
import axios from 'axios'

export default {
  layout: 'flat',
  data() {
    return {
      valid: true,
      mode: 'login',
      showPassword: false,
      password: '',
      pswdRules: [
        (v) => !!v || 'Password is required',
        (v) => (v && v.length > 7) || 'Password must be 8 characters or more'
      ],
      user_name: '',
      userNameRules: [
        (v) => !!v || 'First name is required',
        (v) => (v && v.length >= 2) || 'Name must not be less than a character'
      ]
    }
  },
  methods: {
    submit() {
      if (this.$refs.form.validate()) {
        // Native form submission is not yet supported
        axios.post('/api/submit', {
          name: this.name,
          email: this.email,
          select: this.select,

          checkbox: this.checkbox
        })
      }
    },
    clear() {
      this.$refs.form.reset()
    }
  }
}
</script>
