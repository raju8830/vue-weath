<template>
  <div class="home displa_flax">
    <div id="app">
      <div class="body_part">
        <TodoHeaderComponent></TodoHeaderComponent>
        <TodoListComponent></TodoListComponent>
      </div>
    </div>

  </div>

</template>

<script>


import TodoHeaderComponent from "@/views/component/TodoHeaderComponent";
import TodoListComponent from "@/views/component/TodoListComponent";
export default {
  name: 'Home',
  components: {TodoListComponent, TodoHeaderComponent},
  data(){
    return{
      activeMenu: 0,
      showList : true,
      todos: [
        {
          name : "List First",
          active : 0
        } ,
        {
          name : "List Second",
          active : 0
        }
      ],
      todo: '',
      selectedIndex: null,
      isEditing: false,
      props: ['item']
    }
  },
  methods:{
    deleteTodo(index){
      this.todos.splice(index, 1)
    }
  },

}






</script>
