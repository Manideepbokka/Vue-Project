<template>
<HandlingInput/> 
<AttriBind/>
<CondLoop/>
<FormBinding/>
<ol>
   <TodoItem v-for="item in groceryList" :todo="item" :key="item.id"></TodoItem>
</ol>
</template>

<script>

import HandlingInput from './components/HandlingInput.vue'
import AttriBind from './components/AttriBind.vue'
import CondLoop from './components/CondLoop.vue'
import FormBinding from './components/FormBinding.vue'
import TodoItem from './components/TodoItem.vue'
export default {
  name: 'App',
  components: {
    HandlingInput,
    AttriBind,
    CondLoop,
    FormBinding,
    TodoItem
  },
  data()
  {
    return{
       groceryList: [
        { id: 0, text: 'Vegetables' },
        { id: 1, text: 'Cheese' },
        { id: 2, text: 'Whatever else humans are supposed to eat' }
        ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
