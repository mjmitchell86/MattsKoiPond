<template>
  <v-layout justify-center align-center>
    <v-flex>
      <v-card>
        <v-card-title class="headline">Matt's Pond</v-card-title>
        <v-card-text>
          <div
            class="iframe-container"
            v-if="$moment().tz('America/New_York').isBetween(
              $moment().set({
              hour: 9
              }),
              $moment().set({
              hour: 20,
              minute: 59
              }))"
          >
            <iframe
              type="text/html"
              frameborder="0"
              src="//video.nest.com/embedded/live/LnyOZCfOGJ?autoplay=1"
              allowfullscreen
            ></iframe>
          </div>
          <div v-else>
            <h3>Sorry, this stream is currently offline.</h3>
            <h4>Running hours are 9am - 9pm EST</h4>
            <h4>Thanks for tuning in. Try again tomorrow!!!</h4>
          </div>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
// import { moment } from "@nuxtjs/moment";
export default {};
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
