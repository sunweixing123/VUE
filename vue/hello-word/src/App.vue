<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Test /> -->
    <!-- <List /> -->
    <!-- <TodoList /> -->
    <!-- <Directive /> -->
    <Feather />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Test from './components/Test.vue'
// import List from './components/List.vue'
// import TodoList from './components/TodoList.vue'
// import Directive from './components/Directive.vue'
import Feather from './components/Feather.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    // Test,
    // List,
    // TodoList,
    // Directive,
    Feather,

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
</style>
