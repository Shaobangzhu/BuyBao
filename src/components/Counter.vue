<template>
  <div>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <p><span>{{num}}</span></p>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>

<script>
  export default{
      props:["num"],
      data(){
          return{
              num:0,
          }
      },
      methods:{
          increment(){
              this.$emit("incre");
          },
          decrement(){
              this.$emit("decre");
          },
      }
  }
</script>


