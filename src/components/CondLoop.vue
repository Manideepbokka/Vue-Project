<template>
  <button @click="show=!show">Toggle List</button>
  <button @click="list.push(list.length +1)">Push List</button>
  <button @click="list.pop()">Pop List</button>
  <button @click="list.reverse()">Reverse List</button>
  <ul v-if="show && list.length">
      <li v-for="item of list" :key="item">{{item}}</li>
  </ul>
  <p v-else-if="list.length">List is not empty, but it is hidden!</p>
  <p v-else>List is empty</p>
</template>

<script>
export default {
data()
{
    return{
        show:true,
        list:[1,2,3,4]
    }
}
}
</script>

<style>

</style>