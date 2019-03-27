<template>
  <div id="app">
    <my-servers></my-servers>
  </div>
</template>

<script>
import myServers from "./components/pages/myServers.vue"

export default {
  name: 'app',
  components: {
    'my-servers': myServers
  },

}
</script>

<style>


</style>
