<template>
  <div style="margin: 20px;">
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        <input type="checkbox" :checked="todo.done" @change="toggle(todo)">
        <span :class="{done: todo.done}">{{ todo.text }}</span>
      </li>
    </ul>
    <input type="text" placeholder="タスクを追加" @keyup.enter="addTodo">
  </div>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  computed: {
    todos () {
      return this.$store.state.todos.list
    }
  },
  methods: {
    addTodo (e) {
      this.$store.commit('todos/add', e.target.value)
    },
    ...mapMutations({
      toggle: 'todos/toggle'
    })
  },
  head () {
    return {
      title: 'Todos'
    }
  }
}
</script>

<style>
.done {
  text-decoration: line-through;
}
</style>
