<template>
  <div id="app">
    <HelloWorld msg="search"  v-on:clicked="alert('clicked')"/>
    <div> search results {{result[0]}}</div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  data: function() {
      return {
          result: ['item1']
      }
  },
  components: {
    HelloWorld
  },
    methods: {
        alert() {
            alert('on')
        }
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
