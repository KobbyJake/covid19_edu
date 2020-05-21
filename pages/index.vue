<template>
  <div>
    <v-container mt-8>
      <br />
      <v-row d-flex reverse wrap>
        <v-col class="animated fadeInLeftBig">
          <v-container text-center align-center justify-center class="hero">
            <img src="~assets/medicare.svg" alt="shsc logo" width="400" />
          </v-container>
        </v-col>
        <v-col>
          <p class="font-weight-black display-3 animated fadeInRightBig">
            COVID-19 Educator.
          </p>
          <hr />
          <br />
          <p
            class="font-weight-normal headline animated bounceInRight delay-1000"
          >
            Educating Ghanaian basic school students on the safety precautions
            to prevent COVID-19 infection and also manage infection.
          </p>
          <br />

          <div mt-5>
            <v-dialog v-model="dialog" persistent max-width="600px">
              <template v-slot:activator="{ on }">
                <v-btn
                  outlined
                  rounded
                  color="light-blue lighten-2"
                  class="text-none"
                  v-on="on"
                  ><v-icon left>mdi-account-edit</v-icon>Register</v-btn
                >
                <!-- <v-btn color="primary" dark v-on="on">Open Dialog</v-btn> -->
              </template>
              <v-card shaped dark>
                <v-card-title>
                  <v-icon left large>mdi-account-edit</v-icon>
                  <span>Student Registration</span>
                </v-card-title>
                <hr />
                <v-card-text>
                  <v-form ref="form" v-model="valid">
                    <v-container>
                      <v-row>
                        <v-col cols="12" sm="6" md="6">
                          <v-text-field
                            label="Legal first name*"
                            v-model="student.first_name"
                            required
                            :rules="firstNameRules"
                          ></v-text-field>
                        </v-col>

                        <v-col cols="12" sm="6" md="6">
                          <v-text-field
                            label="Legal last name*"
                            v-model="student.last_name"
                            required
                            :rules="lastNameRules"
                          ></v-text-field>
                        </v-col>

                        <v-col cols="12" sm="6">
                          <v-text-field
                            v-model="student.age"
                            required
                            type="number"
                            max="25"
                            min="4"
                            label="age"
                          ></v-text-field>
                        </v-col>
                        <v-col cols="12" sm="6">
                          <v-select
                            v-model="student.gender"
                            :items="['Male', 'Female']"
                            label="Gender"
                          ></v-select>
                        </v-col>
                        <v-col cols="12">
                          <v-text-field
                            v-model="student.name_of_school"
                            label="Name of school*"
                          ></v-text-field>
                        </v-col>
                        <v-col cols="12" sm="6" md="6">
                          <v-autocomplete
                            v-model="student.region_of_school"
                            :items="[
                              'Oti',
                              'Bono East',
                              'Ahafo',
                              'North East',
                              'Savannah',
                              'Western North',
                              'Western',
                              'Volta',
                              'Greater Accra',
                              'Ashanti',
                              'Central',
                              'Upper East',
                              'Upper West'
                            ]"
                            label="Region of school*"
                            required
                          ></v-autocomplete>
                        </v-col>
                        <v-col cols="12" sm="6" md="6">
                          <v-autocomplete
                            v-model="student.class_of_study"
                            :items="[
                              'Basic 1',
                              'Basic 2',
                              'Basic 3',
                              'Basic 4',
                              'Basic 5',
                              'Basic 6',
                              'JHS 1',
                              'JHS 2',
                              'JHS 3'
                            ]"
                            label="Class of study*"
                            required
                          ></v-autocomplete>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-form>
                  <small>*indicates required field</small>
                </v-card-text>
                <hr />
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    outlined
                    rounded
                    color="default"
                    class="text-none"
                    @click="dialog = false"
                    ><v-icon left>mdi-close</v-icon>Close</v-btn
                  >
                  <v-btn
                    outlined
                    rounded
                    color="light-blue lighten-2"
                    class="text-none"
                    @click="dialog = false"
                    ><v-icon left>mdi-content-save</v-icon>Save</v-btn
                  >
                </v-card-actions>
              </v-card>
            </v-dialog>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'
// import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  data() {
    return {
      dialog: false,
      valid: false,
      student: {
        first_name: '',
        last_name: '',
        age: '',
        gender: '',
        name_of_school: '',
        region_of_school: '',
        class_of_study: ''
      },
      lastNameRules: [
        (v) => !!v || 'Last name is required',
        (v) => (v && v.length <= 2) || 'Name must not be less than a character'
      ],
      firstNameRules: [
        (v) => !!v || 'First name is required',
        (v) => (v && v.length <= 2) || 'Name must not be less than a character'
      ]
    }
  }
  // components: {
  //   Logo,
  //   VuetifyLogo
  // }
}
</script>
<style>
.banner {
  height: 100%;
}
.hero {
  transform: translateY(5%);
}
</style>
