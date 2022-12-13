<template>
  <section id="hero" style="background: red">
    <v-row no-gutters>
      <v-img src="@/assets/whiteboard.jpg" height="100vh">
        <v-row class="fill-height ma-0 text-center">
          <v-col class="align-self-end" cols="12">
            <v-row class="ma-0" align="center" justify="center">
              <v-col cols="2">
                <v-btn rounded class="darken-blur white--text" depressed block>
                  <v-icon left color="indigo">mdi-heart-cog-outline</v-icon>定制
                  Higo
                </v-btn>
              </v-col>
              <v-col cols="2">
                <v-btn rounded class="lighten-blur" depressed block
                  ><v-icon left color="indigo">mdi-video-outline</v-icon>了解
                  Higo</v-btn
                >
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12">
                <v-btn icon class="mb-2">
                  <v-icon color="black">mdi-arrow-down</v-icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-img>
    </v-row>
  </section>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "appMain",
  data: () => ({}),
});
</script>

<style>
.darken-blur {
  background: rgba(23, 26, 32, 0.8) !important;
  backdrop-filter: blur(8px) !important;
}

.lighten-blur {
  background: rgba(244, 244, 244, 0.65) !important;
  backdrop-filter: blur(8px) !important;
}
</style>
