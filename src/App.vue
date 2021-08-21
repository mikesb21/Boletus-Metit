<template>
  <v-app id="app">
    <Nav />
    <router-view />
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import Nav from "./components/common/Nav.vue";

import "./assets/App.scss";

@Component({
  name: "App",
  components: {
    Nav,
  },
})
export default class App extends Vue {}
</script>
