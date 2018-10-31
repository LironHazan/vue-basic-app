<template>
  <div id="app">
    <Search msg="search"  v-on:search="onSearch"/>
    <div v-for="item of vmList"> {{item}}</div>
  </div>
</template>

<script>
import Search from "./components/search/Search.vue";

export default {
  name: "app",
  data: function() {
      return {
          list: ['one', 'too', 'me'],
          vmList: []
      }
  },
  components: {
      Search
  },
    mounted() {
        this.vmList = this.list;
    },
    methods: {
        onSearch(value) {
            console.log(value);
            this.vmList = this.list;
            this.vmList = this.list.filter(item => item.includes(value));
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
