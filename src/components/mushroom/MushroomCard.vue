<template>
  <v-card class="mb-4">
    <v-card-title>{{ title }}</v-card-title>
    <v-card-text> {{ description }}</v-card-text>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component({
  name: "MushroomCard",
})
export default class MushroomCard extends Vue {
  @Prop(String) readonly title!: string;
  @Prop(String) readonly description!: string;
}
</script>
