<template>
  <div>
    <todo-list-item 
      v-for="todo in todos" 
      :key="todo.date"
      :todo="todo">
    </todo-list-item>
  </div>
</template>

<script>
// 절대위치, @ :src의미
import TodoListItem from '@/components/TodoListItem.vue'

import { mapState } from 'vuex'

export default {
  name: 'TodoList',
  components: {
    TodoListItem
  },
  computed: {
    ...mapState(['todos']),
    // todos() {
    //   return this.$store.state.todos
    // }
  },

}
</script>

<style>

</style>
