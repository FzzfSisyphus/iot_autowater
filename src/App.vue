<template>ellowWorld.vue
  <div>
    <img class='gptpic' alt="Vue logo" src="./assets/pic.png">
    <h2>group 2 agriculture </h2>
  </div>
  <RainFall/>
  <WaterInfo/>
</template>

<script>
import RainFall from './components/RainFall.vue';
import WaterInfo from './components/WaterInfo.vue';

export default {
  name: 'App',
  components: {
    RainFall,
    WaterInfo,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.gptpic{
  width: 20%;
  height: 20%;
}
</style>./components/RainFall.vue
