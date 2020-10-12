<template>
  <div id="app">
    <Header />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  </div>
</template>

<script>
import Header from './components/Layouts/header';
import Todos from './components/todos';
export default {
  name: 'App',
  components: {
    Todos, 
    Header
  },
  data(){
    return{
      todos: [
        {
          id: 1,
          title: "Task 1",
          completed: false
        },
        {
          id: 2,
          title: "Task 2",
          completed: false
        },
        {
          id: 3,
          title: "Task 3",
          completed: false
        }
      ]
    }
  },
  methods:{
    deleteTodo(id){
      this.todos = this.todos.filter(todo=> todo.id !== id);
    }
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding:0;
}
body {
  font-family:  Helvetica, Arial, sans-serif;
 line-height:1.4;
}
</style>
