<template>
  <div>
    <v-card shaped dark>
      <v-card-title>
        <v-icon left large>mdi-account-edit</v-icon>
        <span>Student Registration</span>
      </v-card-title>
      <hr />
      <v-form
        ref="form"
        v-model="valid"
        lazy-validation
        name="educov-student"
        method="post"
        data-netlify="true"
        data-netlify-honeypot="bot-field"
      >
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" sm="6" md="6">
                <v-text-field
                  v-model="student.first_name"
                  label="Legal first name*"
                  required
                  :rules="firstNameRules"
                ></v-text-field>
              </v-col>

              <v-col cols="12" sm="6" md="6">
                <v-text-field
                  v-model="student.last_name"
                  label="Legal last name*"
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
                  label="Age"
                  :rules="ageRules"
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
                  required
                  :rules="schoolRules"
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
                  :rules="regionRules"
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
                  :rules="classRules"
                ></v-autocomplete>
              </v-col>
            </v-row>
          </v-container>

          <small>*indicates required field</small>
        </v-card-text>
        <hr />
        <v-card-actions>
          <v-btn
            outlined
            rounded
            color="default"
            class="text-none"
            @click="dialog = false"
            ><v-icon left>mdi-close</v-icon>Close</v-btn
          >
          <v-spacer></v-spacer>
          <v-btn
            outlined
            rounded
            color="default"
            class="text-none"
            @click="clear"
          >
            <v-icon>mdi-backspace</v-icon>Reset
          </v-btn>
          <v-btn
            outlined
            rounded
            color="light-blue lighten-2"
            class="text-none"
            @click="submit"
          >
            <v-icon left>mdi-content-save</v-icon>Submit</v-btn
          >
        </v-card-actions>
      </v-form>
    </v-card>
  </div>
</template>

<script>
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
      ageRules: [
        (v) =>
          (v && Number.isInteger(Number(v))) ||
          'Age must be a positive whole number'
      ],
      schoolRules: [
        (v) => !!v || 'Name of school is required',
        (v) => (v && v.length >= 2) || 'Name must be more than a character'
      ],
      regionRules: [(v) => !!v || 'Region of school is required'],
      classRules: [(v) => !!v || 'Class of study is required'],
      lastNameRules: [
        (v) => !!v || 'Last name is required',
        (v) => (v && v.length >= 2) || 'Name must be more than a character'
      ],
      firstNameRules: [
        (v) => !!v || 'First name is required',
        (v) => (v && v.length >= 2) || 'Name must be more than a character'
      ]
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
  }
}
</script>

<style lang="scss" scoped></style>
