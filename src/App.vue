<template>
  <div id="app">  
    
    <todo-list v-bind:todos="todos"></todo-list>
    <create-todo v-on:add-todo="createTodo"></create-todo>
  </div>
</template>

<script>
import sweetalert from 'sweetalert';
import TodoList from './components/TodoList'
import CreateTodo from './components/CreateTodo'

export default {
  name: 'app',
  components: {
    TodoList,
    CreateTodo
  },
  data () {

    return {
      todos: [{

        title: 'Todo A',
        project: 'Project A',
        done: true
      }, {
        title: 'Todo B',
        project: 'Project B',
        done: false
      }, {
        title: 'Todo C',
        project: 'Project C',
        done: true
      }, {
        title: 'Todo D',
        project: 'Project D',
        done: false
      }, {
        title: 'Todo E',
        project: 'Project E',
        done: true
      }]
    };
  },
  methods: {

    createTodo(titile){
      this.todos.push({
        title,
        done: false
      });
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
