<template>
   <div>
      <ul>
         <TodoItem 
         v-for= "(todo, i) in todos" 
         v-bind:todo="todo" :key=" i" 
         v-bind:index="i"
         v-on:do-remove-todo="removeTodo"
         />
      </ul>
   </div>
</template>

<script>
import TodoItem from '@/components/TodoItem'
export default {
   props:['todos'],
   components: {
      TodoItem
   },
   methods: {
      removeTodo(id) {
         console.log('ASODIJNASODNASOD');
         this.$emit('remove-todo', id)
      }
   }
}
</script>

<style scoped>
   ul {
      list-style: none;
      margin: 0;
      padding: 0;
   }
</style>