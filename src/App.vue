<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- {{msg}} -->

    <!-- pass props to Todos component -->
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos'

export default {
  name: 'App',
  //import components
  components: {
    // HelloWorld
    Todos
  },
  data(){
    return{
      msg: 'Hi asdf',
      todos: [
        {
          id: 1,
          title: 'hi 1',
          completed: false
        },
        {
          id: 2,
          title: 'hi 2',
          completed: false
        },
        {
          id: 3,
          title: 'hi 3',
          completed: false
        },
      ]
    } 
  }
}
</script>

<style scoped>
  #app{
    border: solid red 1px;
  }


</style>
