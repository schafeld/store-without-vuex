<template>
  <div class="fancy-text">
    <p>Fancy Number: {{counter}}</p>
  </div>
</template>

<script>
import { store } from "@/store";

export default {
  computed: {
    counter() {
      return store.count;
    }
  }
};
</script>

<style>
.fancy-text {
  font-family: "Courier New", Courier, monospace;
  color: darkgoldenrod;
  background-color: bisque;
  padding: 1em;
  margin: 2em;
  display: block;
}
</style>
