<template>
  <div class="homepage">
    <h1>Homepage view</h1>
    <div style="width:40%">
      <Chart :chartData="datacollection"></Chart>
    </div>
    
    <canvas id="myChart"></canvas>
  </div>
</template>

<script>
import Chart from '@/components/Chart'
import Store from '../store'
export default {
  props: ['id'],
  name: 'homepage',
  components: {
    Chart
  },
  data () {
    return {
      datacollection: {}
    }
  },
  beforeMount () {
    if (Store.graphConfig) {
      Store.graphConfig.labels.push('Random')
      Store.graphConfig.datasets[0].data.push(40)
      this.datacollection = Store.graphConfig
      console.log(this.datacollection.datasets[0].data)
    } else {
      this.fillData()
    }
  },
  mounted () {
    // window.displayGraph()
    setInterval(this.fillData, 1000)
  },
  destroyed () {
    console.log('Destroy')
    Store.graphConfig = this.datacollection
  },
  methods: {
    fillData () {
      this.datacollection = {
        labels: ['Red', 'Green', 'Blue'],
        datasets: [{
          labels: 'Sample Dataset',
          data: [],
          backgroundColor: 'rgba(255, 0, 0, 1)',
          borderColor: 'rgba(255,99,132,1)'
        }]
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
