<template>
  <div id="app">
    <img class="App-logo" alt="Vue logo" src="./assets/logo.png">
    <div v-if="show">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
    <div v-else>
      <Users />
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Users from './components/Users.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Users
  },
  data() {
    return {
    show : false,
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


.App-logo {
  animation: App-logo-spin infinite 20s linear;
  height: 20vmin;
}
@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
