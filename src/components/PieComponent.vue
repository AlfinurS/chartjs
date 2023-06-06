<script>
import { Pie } from 'vue-chartjs'

export default {
  extends: Pie,
  data: () => ({
    data: {
      labels: ['Red', 'Orange', 'Yellow', 'Green', 'Blue'],
      datasets: [{
          label: 'My First Dataset',
          data: [300, 50, 100, 40],
          backgroundColor: [
            'rgb(255, 99, 132)',
            'rgb(54, 162, 235)',
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
