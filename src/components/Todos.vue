<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      
      <TodoItem :todo="todo" @del-todo="$emit('del-todo', todo.id)"/>
    </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem';

export default {
  name: "Todos",
  props: ["todos"],
  components: {
    TodoItem
  },
  methods: {
    
  }
}
</script>

<style scoped>

</style>