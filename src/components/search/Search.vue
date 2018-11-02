<template>
  <div class="hello">
    {{msg}}
    <input v-model="text" @keyup.enter="notifySearch()"/>
  </div>
</template>

<script>
export default {
  name: "SearchComponent",
  // In components the data returns from a factory function so that you could use
  // the component on several elements and have a different state for each
  data: function() {
      return {
          text: ''
      }
  } ,
  props: {
    msg: String
  },
    methods: {
        notifySearch() {
            // This is how you notify the parent that
            this.$emit('search', this.text);
        }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
