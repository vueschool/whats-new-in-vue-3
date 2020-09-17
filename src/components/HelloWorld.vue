<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <button @click="showMessage = !showMessage">Toggle Message</button>
    <button @click="showModal = true">Show Modal</button>

  </div>
  <teleport to="#modal-container" :disabled="false">
    <BaseModal v-if="showModal">
      <h1>Hi Vue School</h1>
      <button @click="showModal = false">Close</button>
    </BaseModal>
  </teleport>


  <teleport to="#purple-box">
    <p v-if="showMessage">Hello from HelloWorld</p>
  </teleport>
</template>

<script>
import BaseModal from "@/components/BaseModal";
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {BaseModal},
  data () {
    return {
      showMessage: true,
      showModal: false
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
