<template>
  <v-layout justify-center align-center>
    <v-flex>
      <v-card>
        <v-card-title class="headline">Matt's Pond</v-card-title>
        <v-card-text>
          <div class="iframe-container" v-if="checkTime()">
            <iframe
              type="text/html"
              frameborder="0"
              src="//video.nest.com/embedded/live/LnyOZCfOGJ?autoplay=1"
              allowfullscreen
            ></iframe>
          </div>
          <div v-else>
            <h3>Sorry, this stream is currently offline. Check back soon!</h3>
          </div>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  methods: {
    checkTime() {
      return true;
    }
  }
};
</script>

<style scoped>
.iframe-container {
  overflow: hidden;
  padding-top: 56.25%;
  position: relative;
}

.iframe-container iframe {
  border: 0;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}
</style>
