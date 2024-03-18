<template>
  <div class="container">
    <canvas ref="chartCanvas"></canvas>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import { Chart, registerables } from 'chart.js';

export default {
  setup() {
    const chartCanvas = ref(null);
    let myChart = null;

    onMounted(() => {
      // Initialize Chart.js
      Chart.register(...registerables);

      // Get the canvas element
      const ctx = chartCanvas.value.getContext('2d');

      // Define chart data
      const data = {
        labels: [ '2024/3/1','2024/4/1','2024/5/1','2024/6/1','2024/7/1','2024/8/1','2024/9/1',
                    '2024/10/1','2024/11/1','2024/12/1','2025/1/1','2025/2/1','2025/3/1',
                    '2025/4/1','2025/5/1','2025/6/1','2025/7/1'] ,
        datasets: [{
          label: 'Rainfall Prediction',
          data: [186.03,205.84,284.71,261.41,246.85,245.26,
                               191.43,232.86,169.07,175.8,159.39,232.73,246.61,
                               257.62,379.23,202.02,278.05],
          borderColor: 'rgba(75, 192, 192, 1)',
          borderWidth: 2,
          fill: false
        }]
      };

      // Create the chart
      myChart = new Chart(ctx, {
        type: 'line',
        data: data,
        options: {
          scales: {
            y: {
              beginAtZero: false
            }
          }
        }
      });
    });

    return { chartCanvas,myChart };
  }
};
</script>

<style scoped>
/* Add any custom styles here */
.container{
  height: 40%;
  width: 60%;
  margin: 0 auto;
}
</style>
