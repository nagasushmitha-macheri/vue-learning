<template>
  <div id="app">
    {{todos}}
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  },
  data(){
    return{
      todos: [
        {
          id: 1,
          title: "Brush teeth",
          completed: false
        },
        {
          id: 1,
          title: "Brush teeth",
          completed: false
        },
        {
          id: 1,
          title: "Brush teeth",
          completed: false
        }
      ]
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
