<template>
  <div v-if="$parent.showList" class="todo_list_component">
    <ul class="order_list_part" style="list-style: none">
      <li v-for="(todo, index) in $parent.todos" :key="index">
        {{ index+1 }}.
        <input v-model="todo.active" class="input_binding"
               type="checkbox"/>
        <span :class="todo.active ? 'active' : '' || index == 0 ? 'first_child': '' || index == $parent.todos.length -1 ? 'last_child': ''" class="active_part">{{ todo.name }}</span>

        <button @click="editTodo(index, todo)">Edit</button>

        <button @click="deleteTodo(index)" >Delete</button>

      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TodoListComponent",
  methods:{
    editTodo(index, todo){
      this.$parent.todo = todo.name
      this.$parent.selectedIndex = index
      this.$parent.isEditing = true
    },
    deleteTodo(index){
      this.$parent.todos.splice(index, 1)
    }
  }
}
</script>

<style scoped>

</style>