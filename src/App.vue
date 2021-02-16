<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  created() {
    this.$http.get('https://randomuser.me/api/')
        .then((response) => {
            console.log(response.data)
        });
  }
}
</script>

<style>
body {
  background-color: gray;
}
</style>
