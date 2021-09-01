<template>
  <div class="todo_header_component">
    <div class="todoListContainer">
      <h2 id="title">{{ $parent.ListHeader }}</h2>

      <div class="input_part">
        <div v-if="!$parent.isEditing" class="input_part">
          <input type="text" v-model="todo" placeholder="Add To Do Any Thing">
          <input type="submit" value="add" @click="storeTodo">
        </div>


        <div v-else>
          <input type="text" v-model="$parent.todo">
          <input type="submit" value="update" @click="updateTodo">
        </div>
      </div>


    </div>
  </div>
</template>

<script>






export default {
  name: "TodoHeaderComponent",
  data() {
    return {
      todo : "",

    }
  },
  methods:{
    storeTodo(){
      if(this.todo){
        let data =  {
          name :this.todo,
          active : 0
        }
        this.$parent.todos.push(data)
      }
      this.todo =''
    },
    updateTodo(){
      this.$parent.todos[this.$parent.selectedIndex].name = this.$parent.todo
      this.$parent.isEditing = false
    }
  }
}


</script>
