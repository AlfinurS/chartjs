<script>

import { Pie } from 'vue-chartjs'


export default {
  extends: Pie,
  data: () => ({
    data: {
      labels: ['Электроника и бытовая техника', 'Мебель и товары для дома', 'Одежда и обувь', 'Продукты питания', 'Товары для красоты и здоровья'],
      datasets: [{
          data: [22, 17.7, 13.9, 13.5, 7.5],
          backgroundColor: [
            'rgb(111, 106, 248)',
            'rgb(84, 116, 185)',
            'rgb(48, 73, 119)',
            'rgb(144, 164, 205)',
            'rgb(120, 152, 224)'
          ],
          hoverOffset: 4,
          borderWidth: 1,
        }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      legend: {
              display: true,
              position: "right",
              labels: { 
                fontColor: 'rgb(25, 22, 81)',
                boxWidth:30
                }
          },
      title: {
              display: true,
              text: 'Категории покупок',
              fontSize: 14,
              padding: 18
          }
    }
  }),

  mounted () {
    this.renderChart(this.data, this.options)
  }
}
</script>
