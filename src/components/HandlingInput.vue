<template>
  <h1>{{msg}}</h1>
  <button @click="reverse" >Reverse Message</button>
  <button @click="msg+='!'" >Append "!"</button>
</template>

<script>
export default {
data(){
    return {
        msg:'Hello World!'
    }
},
methods:
{
reverse()
{
    this.msg=this.msg.split('').reverse().join('')
}
}
}
</script>

<style>

</style>