<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md8>
      <v-card>
        <v-card-title class="headline">Matt's Pond</v-card-title>
        <v-card-text>
          <div class="resp-container">
            <iframe
              class="resp-iframe"
              src="https://www.youtube.com/embed/dQw4w9WgXcQ"
              gesture="media"
              allow="encrypted-media"
              allowfullscreen
            ></iframe>
          </div>
          <!-- <iframe
            type="text/html"
            frameborder="0"
            width="720"
            height="591"
            src="//video.nest.com/embedded/live/3bCNu0yep2?autoplay=1"
            allowfullscreen
          ></iframe>-->
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
.resp-container {
  position: relative;
  overflow: hidden;
  padding-top: 56.25%;
}
.resp-iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}
</style>
