<template>
  <div class="yo">
    <div v-bind:key="todo.id" v-for="todo in todos">
        <TodoItem v-bind:todo="todo" v-on:del-todo="${emit('del-todo', todo.id)"/>
    </div>
  </div>
</template>

<script>

import TodoItem from './TodoItem.vue'

export default {
    components: {
        TodoItem
    },
    name: "todos",
    props: ["todos"]
};
</script>
    
    
<style scoped>
  .yo{
  border: solid black

  }

</style>