<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <TodoApp msg="Welcome to Your Vue.js App"/>
  <p>--------------------------------------</p>
  <todo-app-with-composition/>
</template>

<script>
import TodoApp from './components/TodoApp.vue'
import TodoAppWithComposition from './components/TodoAppWithComposition.vue'

export default {
  name: 'App',
  components: {
    TodoApp,
    TodoAppWithComposition
  },
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
