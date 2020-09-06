<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <SomeButtons/>
  </div>
</template>

<script>
import SomeButtons from "@/components/SomeButtons";
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {SomeButtons}
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
