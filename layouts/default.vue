<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-if="!isMobile()" v-text="title" />
      <v-toolbar-title v-else v-text="altTitle" />
      <v-spacer />
    </v-app-bar>
    <v-content class="background" :style="{ backgroundImage: `url(${backgroundUrl})` }">
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import backgroundUrl from "~/static/koi-fish-1.jpg";
export default {
  methods: {
    isMobile() {
      if (
        /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
          navigator.userAgent
        )
      ) {
        return true;
      } else {
        return false;
      }
    }
  },
  data() {
    return {
      backgroundUrl: backgroundUrl,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-fish",
          title: "Matt's Pond",
          to: "/"
        },
        {
          icon: "mdi-fish",
          title: "Sandi and Jeff's Pond",
          to: "/sandiandjeff"
        }
      ],
      title: "Welcome To Matt's Collection Of Koi Streams",
      altTitle: "Welcome To My Koi Streams"
    };
  }
};
</script>
