<template>
  <div id="app">
    <p>Count: {{ count }}</p>
    <button @click="setCount(count + 1);">+ 1</button>
    <button @click="setCount(count - 1);">- 1</button>
    <fancy-counter/>
    <p>
      How to provide a simple store functionality
      without using VueX. Sources:
    </p>
    <ul>
      <li>https://vuejs.org/v2/api/#Vue-observable</li>
      <li>https://vuedose.tips/tips/creating-a-store-without-vuex-in-vue-js-2-6</li>
    </ul>
  </div>
</template>

<script>
import FancyCounter from "@/components/FancyCounter";
import { store, mutations } from "./store";

export default {
  components: { FancyCounter },
  computed: {
    count() {
      return store.count;
    }
  },
  methods: {
    setCount: mutations.setCount
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
