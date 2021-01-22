<template>
  <div id="app">
    <Header/>
    <router-view/>
  </div>
</template>
<script>
import Header from "./components/Header";
import Play from './components/Play'
export default {
  name: 'app',
  components: {
    Header,
    Play,
  }
}
</script>

<style>
  @import './css/main.css';
</style>
