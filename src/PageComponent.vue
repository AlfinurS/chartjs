<template>
<div class="container"> 
  <h1 class="headline">Онлайн-продажи в России</h1>
    
  <div class="section">
      <PieComponent class="w-pie"/>
      <ChartComponent class="w-chart"/>
  </div>
  <div class="section">
      <DoughnutComponent class="w-doughnut"/>
      <RandomChart class="w-line"/>
  </div>
</div>
</template>


<script>
import ChartComponent from './components/ChartComponent.vue'
import RandomChart from './components/RandomChart.vue'
import PieComponent from './components/PieComponent.vue'
import DoughnutComponent from './components/DoughnutComponent.vue'

export default {
  name: 'PageComponent',
  components: {
    PieComponent,
    ChartComponent,
    RandomChart,
    DoughnutComponent
  }
}
</script>

<style>
.container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.section {
  display: flex;
  justify-content: center;
  width: 100%;
  margin-bottom: 40px;

}
.w-pie {
  max-width: 600px;
  width: 100%;
  padding: 38px;
  box-shadow: 0px 5px 7px -2px rgba(26, 21, 32, 0.18);
  border-radius: 8px;
  background-color: #FFFFFF;
  margin-right: 20px;
}
.w-chart {
  max-width: 500px;
  width: 100%;
  padding: 20px;
  box-shadow: 0px 5px 7px -2px rgba(26, 21, 32, 0.18);
  border-radius: 8px;
  background-color: #FFFFFF;
}

.w-line {
  max-width: 500px;
  width: 100%;
  padding: 20px;
  box-shadow: 0px 5px 7px -2px rgba(26, 21, 32, 0.18);
  border-radius: 8px;
  background-color: #FFFFFF;
}

.w-doughnut {
  max-width: 500px;
  width: 100%;
  padding: 20px;
  box-shadow: 0px 5px 7px -2px rgba(26, 21, 32, 0.18);
  border-radius: 8px;
  background-color: #FFFFFF;
  margin-right: 20px;

}

.headline {
  color: #191651;
  font-size: 28px;
  margin-bottom: 30px;
}
</style>