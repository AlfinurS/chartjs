<template>
<div class="container"> 
    <h1 class="headline">Онлайн-продажи в России</h1>
    
    <h3 class="subtitle">Категории покупок</h3>

    <PieComponent class="w-75"/>

    <h3 class="subtitle">Обновление графиков</h3>
    <RandomChart class="w-75" />

    <h3 class="subtitle">Круг</h3>
    
    <ChartComponent class="w-75" />
    <h3 class="subtitle">Бублик</h3>
    <DoughnutComponent class="w-75"/>
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
.w-75 {
  width: 35%;
  margin-left: 20px;
  margin-right: auto;
  box-shadow: 0px 5px 7px -2px rgba(26, 21, 32, 0.18);
  border-radius: 8px;
  background-color: #FFFFFF;
}
.headline {
  text-align: center;
  color: #191651;
  font-size: 40px;
}
.subtitle {
  font-size: 20px;
  color: #191651;
  margin-top: 60px;
  text-align: left;
}
</style>