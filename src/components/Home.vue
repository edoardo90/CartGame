<template>
  <div class="hello">
    <h1>Home</h1>
    <p>
      This is the Home!
    </p>
      <span v-bind:title="message">
        Let me tell you: {{ message }}
      </span>
      <li v-for="num in numbers">
        number: {{ num }}
      </li>

      <button v-on:click="removeNumber"> remove </button>
      <button v-on:click="addNumber"> add </button>

      <br/><br />
      <input v-model="message">

    <br /> Speed...

      <Play speed=10 :secret="message"></Play>


  </div>
</template>
<script>
import Play from './Play'
export default {
  name: 'Home',
  data () {
    return {
      message: "a secret ~  " + (new Date()).toLocaleTimeString(),
      numbers: [1,2,3]
    }
  },
  components: {
    Play
  },
  methods: {
    removeNumber: function() {
      this.numbers.splice(0,1 )
    },
    addNumber: function()  {
      this.numbers.push(33)
    }
  }
}
</script>
<style scoped>
</style>
