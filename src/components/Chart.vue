<script>
import { Line, mixins } from 'vue-chartjs'

export default Line.extend({
  props: ['chartData'],
  mixins: [mixins.reactiveProp],
  data () {
    return {
      options: {
        responsive: true,
        animateScale: true,
        title: {
          display: true,
          text: 'Sample bar chart'
        },
        scales: {
          xAxes: [{
            ticks: {
              beginAtZero: true
            },
            barPercentage: 0.9
          }]
        }
      }
    }
  },
  mounted () {
    this.renderChart(this.chartData, this.options)
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
