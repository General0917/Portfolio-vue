<script>
import { Doughnut } from 'vue-chartjs'
export default {
  extends: Doughnut,
  props: {
    chartdata: {
      type: Object,
      default: null
    }
  },
  data: () => ({
    options: {
      responsive: true,
      maintainAspectRatio: false,
      animation: false,
      tooltips: {
        enabled: false
      },
      hover: {
        mode: null
      }
    }
  }),
  mounted() {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>