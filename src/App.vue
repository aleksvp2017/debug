<template>
  <div id="app">
    <input v-model="fibonacciLimit">
    <button @click="showAlert">Calculate Fibonacci</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      fibonacciLimit: 0,
    }
  },
  methods:{
    showAlert(){
      var sequence = []
      for (var ind = 0; ind < this.fibonacciLimit; ind++){
        if (sequence.length <= 2){
          sequence.push(ind)
        }
        else{
          var fibonacci = 0
          fibonacci = sequence[ind-1] + sequence[ind-2]
          sequence.push(fibonacci)
        }
      }
      alert('Fibonacci:' + sequence)
    }
  }
}
</script>

<style>
</style>
