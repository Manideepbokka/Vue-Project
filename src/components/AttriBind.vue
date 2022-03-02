<template>
  <p><span :title="message" >Hover your mouse over it to dynamically bound title!</span></p>
  <p :class="{red: isRed}" @click="toggleRed"> This should be red... but click me to toggle it.</p>
  <p :style="{ color }" @click="toggleColor">
    This should be green, and should toggle between green and blue on click.
  </p>
</template>

<script>
export default {
data()
{
    return {
        message:"Hi Manideep!",
        isRed:true,
        color:'crimson'

    }
},
methods:
{
    toggleRed()
    {
        this.isRed=!this.isRed
    },
    toggleColor()
    {
        this.color=this.color==='crimson'?'blue':'crimson'
    }
}
}
</script>

<style>
.red{
    color:red;
}
</style>