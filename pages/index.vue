<template>
  <v-layout justify-center align-center>
    <v-flex>
      <v-card>
        <v-card-title class="headline">Matt's Pond</v-card-title>
        <v-card-text>
          <div class="iframe-container">
            <iframe
              type="text/html"
              frameborder="0"
              src="//video.nest.com/embedded/live/3bCNu0yep2?autoplay=1"
              allowfullscreen
            ></iframe>
          </div>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

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
