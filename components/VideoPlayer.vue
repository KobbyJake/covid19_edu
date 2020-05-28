<template>
  <div>
    <v-playback :url="link" loop auto-play="play"></v-playback>
  </div>
</template>

<script>
import vPlayBack from 'v-playback'
export default {
  props: {
    link: {
      type: String,
      default: '/handwashing.mp4'
    }
  },
  components: {
    'v-playback': vPlayBack
  }
}
</script>
