<template>
  <div id="app">
    <div class="container">
      <bar-chart :chart-data="chartData" :options="options"></bar-chart>
    </div>
    <div class="container">
      <bar-chart :chart-data="chartData" :options="options"></bar-chart>
    </div>
    <div class="container">
      <bar-chart :chart-data="chartData" :options="options"></bar-chart>
    </div>
    <div class="container">
       <bar-chart :chart-data="chartData" :options="options"></bar-chart>
    </div>    
  </div>
</template>

<script>
import barChart from './components/bar-chart.vue'

export default {
  name: 'app',
  components: {
    barChart: barChart
  },
  data() {
    return {
      chartData: {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
        datasets: [
          {
            label: 'GitHub Commits',
            backgroundColor: '#f87979',
            data: [40, 20, 12, 39, 10, 40, 39, 80, 40, 20, 12, 11]
          }
        ]
      },
      options: {
        plugins: {
          deferred: {
            yOffset: '50%',
            delay: 3000
          }
        }
      }
    }
  }
}
</script>

<style>
.container {
  width: 500px;
  height: 500px;
  margin-top: 200px;
}
</style>
