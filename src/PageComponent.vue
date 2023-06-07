<template>
<div>
    <h1>Онлайн-продажи в России</h1>
    
    <h3>Категории покупок</h3>

    <PieComponent class="w-75"/>

    <h2>Обновление графиков</h2>
    <RandomChart class="w-75" />
    <h2>Круг</h2>
    
    <ChartComponent class="w-75" />
    <h2>Бублик</h2>
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
  width: 55%;
  margin-left: auto;
  margin-right: auto;
}
</style>