<template>
  <h1>here is water info</h1>
  <div class="total_container"> 
    <div>
      <img :src="sunflowerURL.url">
    </div>
    <div>
      <h2> Sat Mar 16 12:12:28 2024  Dry </h2>
      <h2>  Sat Mar 17 12:12:28 2024  Dry</h2>
      <h2>  Sat Mar 18 12:12:28 2024  Water</h2>
    </div>
    <div >
      <img class="waterimg" :src="waterURL.url">
    </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      sunflowerURL:{url:require('../assets/sunflower.gif')},// Replace with your GIF path
      waterURL:{url:require('../assets/water.gif')}
    };
  },
};
</script>

<style scoped>
.total_container{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
}
.waterimg{
  width: 50%;
  height: 70%;
}
</style>