<template>
  <v-app style="font-family: futura">
    <v-app-bar app color="transparent" flat fixed>
      <v-btn text class="font-weight-bold">HiGo</v-btn>
      <v-spacer />
      <v-btn text>探索·Explore</v-btn>
      <v-btn text>模版</v-btn>
      <v-btn text>场景解决方案</v-btn>
      <v-btn text>体验DEMO</v-btn>
      <v-spacer />
      <v-btn text>在线商店</v-btn>
      <v-btn text>账户</v-btn>
      <v-btn text @click="right = !right">导航栏</v-btn>
    </v-app-bar>
    <v-main class="pa-0">
      <router-view />
    </v-main>
    <v-navigation-drawer right app v-model="right" absolute temporary>
      <v-toolbar flat>
        <v-spacer />
        <v-btn text small color="black" @click="right = false">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-toolbar>
      <v-list nav dense class="mx-2 mt-0">
        <v-list-item v-for="(item, i) in items" :key="i" link>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"> </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "App",
  data: () => ({
    right: false,
    items: [
      {
        title: "长期支持",
      },
      {
        title: "Milestone",
      },
      {
        title: "找到我们",
      },
      {
        title: "问题解答",
      },
    ],
  }),
});
</script>

<style>
/**
隐藏overflow-y轴
*/
html {
  overflow-y: auto;
}

.lighten-blur {
  background: rgba(244, 244, 244, 0.65) !important;
  backdrop-filter: blur(8px) !important;
}
</style>
