<template>
  <div class="hello">
    <h1>PLAY</h1>
    <p>
      PRESS buttons and play {{ this.$props.secret }}
    </p>
    <button v-on:click="sayLoud"> Go left </button>
  </div>
</template>
<script>
export default {
  name: 'Play',
  props: {
    speed: {
      type: Number, required: false
    },
    secret: {
      type: String, required: false
    }
  },
  methods: {
    sayLoud(what) {
      console.log("whhhatttt: ", what,
      "oh and btw speed is: ", this.speed,
          (this.secret ?  ("secret" + this.secret)
                  :  "no secrets"
          ));
    }
  }
}
</script>
<style scoped>
</style>
