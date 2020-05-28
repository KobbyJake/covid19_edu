<template>
  <v-row class="fill-height wall" align="center" justify="center">
    <v-card class="mx-auto" max-width="500">
      <v-card-title primary-title>
        <p class="display-1 text--primary text-center">
          Certificate of Participation
        </p>
      </v-card-title>
      <v-card-text>
        <hr />
        <p class="display-2 text--primary text-center">
          Recipient Name
        </p>
        <div class="text--primary text-center">
          Has completed the study of content on
        </div>
        <p class="display-1 text--primary text-center">
          COVID-19
        </p>
        <div class="text--primary text-left">On this day {{ new Date() }}</div>
        <br />
        <div class="text--primary text-right">
          ...Signed...
        </div>
        <hr />
      </v-card-text>
      <v-card-actions>
        <v-btn outlined large class="text-none" @click="print">
          Print
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-row>
</template>

<script>
export default {
  methods: {
    print() {
      window.print()
    }
  }
}
</script>

<style>
.wall {
  background: url(~assets/cool-background.png) no-repeat center fixed;
  background-size: cover;
}
</style>
