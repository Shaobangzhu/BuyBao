<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <Counter v-bind:num="num" v-on:incre="increment" v-on:decre="decrement"></Counter>
    <p>parent:{{num}}</p>
  </div>
</template>

<script>

  import Counter from './Counter'

  export default {
    name: 'HelloWorld',
    data () {
      return {
        num:10,
        msg: 'Welcome to Your Vue.js App'
      }
    },
    components:{
        Counter
    },
    methods:{
        increment(){
            this.num++;
        },
        decrement(){
            this.num--;
        }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}
</style>
