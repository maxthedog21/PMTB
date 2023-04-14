<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { ref } from "vue";
import Header from "./components/Header.vue";
</script>

<template>
  <v-app>
      <v-main>
              <Header title="Vue Sculpt" version="Beta V1"></Header>
              <v-row>
                  <v-col cols="6">
                  </v-col>
                  <v-col cols="6">
                  </v-col>
              </v-row>
      </v-main>
  </v-app>
</template>
<style scoped>
.logo.vite:hover {
  filter: drop-shadow(0 0 2em #747bff);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #249b73);
}
</style>
