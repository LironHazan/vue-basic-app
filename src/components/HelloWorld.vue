<template>
  <div class="hello">
    <input v-model="text" @keyup.enter="enterClicked()"/>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: function() {
      return {
          text: ''
      }
  } ,
  props: {
    msg: String
  },
    methods: {
        enterClicked() {
            this.$emit('clicked', this.text);
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
