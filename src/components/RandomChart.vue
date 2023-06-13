<template>
  <div >
    <line-chart :chart-data="datacollection"></line-chart>
    <!-- <button @click="fillData()">Обновить</button> -->
  </div>
</template>

<script>
  import LineChart from './LineChart.js'

  export default {
    components: {
      LineChart
    },
    data () {
      return {
        datacollection: null
      }
    },
    mounted () {
      this.fillData()
    },
    methods: {
      fillData () {
        this.datacollection = {
          labels: ['2023', '2022'],
          datasets: [
            {
              label: 'Wildberries №2',
              backgroundColor: '#79f879',
              data: [41, 47]
            },
            {
              label: 'Ozon №1',
              backgroundColor: '#f87979',
              data: [63, 59]
            }, 
          ]
        }
      },
    }
  }
</script>

<style>
</style>
