<template>
    <div class="item">
        <p>{{todo.title}}</p>
        <input type="checkbox" v-on:change="markComplete">

        <!-- this is a click event with a parameter -->
        <!-- it basically emits a function to the parent component, then the parent component can emit it up to the grandparent component -->
        <button @click="$emit('del-todo', todo.id)">delete</button>
    </div>
</template>

<script>
export default {
    name: 'tod item',
    props: ["todo"],
    methods: {
        markComplete(){
            console.log('123')
            this.props.completed = !this.props.completed
        }
    }
}
</script>

<style scoped>

  .item{
    border: solid green 1px;
  }

</style>