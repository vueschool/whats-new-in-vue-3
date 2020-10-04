<template>
  <div class="hello">
    <h1>Vue 3</h1>
    <h2>Reactivity</h2>
    {{website}}
    <hr>
    <button @click="addTwitter">Add Twitter</button>
    <button @click="removeLink">Remove Link</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      website: {
        name: 'Vue School',
        link: 'vueschool.io'
      }
    }
  },
  methods: {
    addTwitter () {
      this.website.twitter = '@vueschool_io'
    },
    removeLink () {
      delete this.website.link
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
  font-size: 3em;
}
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
