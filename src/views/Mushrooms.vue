<template>
  <v-container class="mushrooms" fluid>
    <h1 class="pb-10">Mushrooms</h1>
    <MushroomCard
      v-for="mushroom in mushrooms"
      :key="mushroom.id"
      :title="mushroom.name"
      :description="mushroom.description"
    />
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import MushroomCard from "../components/mushroom/MushroomCard.vue";

import { v4 as uuidv4 } from "uuid";

@Component({
  name: "Mushrooms",
  components: {
    MushroomCard,
  },
})
export default class Mushrooms extends Vue {
  mushrooms = new Array(4).fill({
    id: uuidv4(),
    name: "Mushroom",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  });
}
</script>
