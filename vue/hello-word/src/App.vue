<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Test /> -->
    <!-- <List /> -->
    <!-- <TodoList /> -->
    <Directive />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Test from './components/Test.vue'
// import List from './components/List.vue'
// import TodoList from './components/TodoList.vue'
import Directive from './components/Directive.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    // Test,
    // List,
    // TodoList,
    Directive,

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
