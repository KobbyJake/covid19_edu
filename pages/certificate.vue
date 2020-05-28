<template>
  <v-row class="fill-height" align="center" justify="center">
    <v-card class="mx-auto" max-width="500">
      <v-card-title primary-title>
        <p class="display-1 text--primary">
          Certificate of Participation
        </p>
      </v-card-title>
      <v-card-text>
        <div>Word of the Day</div>
        <p class="display-1 text--primary">
          This is to certify that
        </p>
        <p>Student</p>
        <div class="text--primary">
          Has completed the study of content on COVID-19
        </div>
      </v-card-text>
      <v-card-actions>
        <v-btn text color="deep-purple accent-4" @click="print()">
          Print Certificate
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-row>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
