<template>
<div class="container"> 
  <h1 class="headline">Онлайн-продажи в России</h1>
  <div class="section">
    <div class="item">
      <ChartComponent class="w-chart"/>
    </div>
    <div class="list">
      <MiniDoughnutComponent class="mini-doughnut"/>
      <OzonDoughnutComponent class="mini-doughnut"/>
      <WilDoughnutComponent class="mini-doughnut"/>
      <VkusDoughnutComponent class="mini-doughnut"/>
    </div>
  </div>

  <div class="section">
    <ItemCardComponent 
      v-for="shop in shops"
      :key="shop.id"
      :dataProps="shop">
    </ItemCardComponent>
  </div>

  <div class="section">
    <div class="item">
      <PieComponent class="w-pie"/>
    </div>
    <div class="item">
      <LineComponent class="w-miniLine"/>
    </div>
  </div>
  <div class="section">
    <div class="item">
      <DoughnutComponent class="w-doughnut"/>
    </div>
    <div class="item">
      <RandomChart class="w-line"/>
    </div>
  </div>
</div>
</template>


<script>

import ItemCardComponent from './components/ItemCardComponent.vue'
import ChartComponent from './components/charts/ChartComponent.vue'
import RandomChart from './components/charts/RandomChart.vue'
import PieComponent from './components/charts/PieComponent.vue'
import LineComponent from './components/charts/LineComponent.vue'
import DoughnutComponent from './components/charts/DoughnutComponent.vue'
import MiniDoughnutComponent from './components/charts/MiniDoughnutComponent.vue'
import OzonDoughnutComponent from './components/charts/OzonDoughnutComponent.vue'
import WilDoughnutComponent from './components/charts/WilDoughnutComponent.vue'
import VkusDoughnutComponent from './components/charts/VkusDoughnutComponent.vue'


export default {
  name: 'PageComponent',
  components: {
    ItemCardComponent,
    PieComponent,
    ChartComponent,
    RandomChart,
    LineComponent,
    DoughnutComponent,
    MiniDoughnutComponent,
    OzonDoughnutComponent,
    WilDoughnutComponent,
    VkusDoughnutComponent
  },

  data() {
    return {
      shops: [
          {
            id: 1,
            name: "Сбермаркет",
            profit: 103.5,
          },
          {
            id: 2,
            name: "Вкусвилл",
            profit: 91.2,
          },
          {
            id: 3,
            name: "Самокат",
            profit: 82.5,
          },
          {
            id: 4,
            name: "Ozon",
            profit: 58.1,
          },
          {
            id: 5,
            name: "Wildberries",
            profit: 57.2,
          },
        ]
    }
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
.list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px; 
  box-shadow: 0px 5px 7px -2px rgba(222, 195, 255, 0.18);
  border-radius: 8px;
  background-color: #FFFFFF;
  padding: 12px 18px;
}

.item {
  display: flex;
  box-shadow: 0px 5px 7px -2px rgba(26, 21, 32, 0.18);
  border-radius: 8px;
  background-color: #ffffff;
  padding: 22px;
  margin-right: 20px;
}
.w-pie {
  max-width: 300px;
}
.w-chart {
  width: 600px;
}

.w-line {
  max-width: 500px;
}

.w-miniLine {
  max-width: 600px;
}
.w-doughnut {
  max-width: 300px;
}

.mini-doughnut {
  max-width: 140px;
  max-height: 200px;
  width: 100%;
}
.headline {
  color: #191651;
  font-size: 28px;
  margin-bottom: 30px;
}
</style>