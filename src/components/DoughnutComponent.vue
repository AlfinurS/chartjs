<script>
import { Doughnut } from 'vue-chartjs'

export default {
  extends: Doughnut,
  data: () => ({
    data: {
      labels: ['Сбермаркет', 'Вкусвилл', 'Самокат', 'Ozon', 'Wildberries'],
      datasets: [{
          label: 'My First Dataset',
          data: [103.5, 91.2, 82.5, 58.1, 57.2],
          backgroundColor: [
            'rgb(255, 99, 132)',
            'rgb(54, 162, 235)',
            'rgb(205, 205, 86)',
            'rgb(255, 205, 86)',
            'rgb(245, 200, 82)'
          ],
          hoverOffset: 4
        }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false
    }
  }),

  mounted () {
    this.renderChart(this.data, this.options)
  }
}
</script>
