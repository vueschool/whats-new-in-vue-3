<template>
  <div class="hello">
    <h1>Vue 3</h1>
    Username: {{username}}
    Pass: {{password}}
    <hr>

    <LoginForm
      v-model:username="username"
      v-model:password="password"
    />
  </div>
</template>

<script>
import LoginForm from "@/components/LoginForm";
export default {
  components: {LoginForm},
  data () {
    return {
      username: null,
      password: null
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
