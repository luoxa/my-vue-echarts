<template>
  <div id="app">
    <div class="ec-box">
            <mychart
            chart-type="bar"
            chart-dimensions="['product', '2015', '2016', '2017']"
            chart-dataset-source="[{product: 'Matcha Latte', '2015': 43.3, '2016': 85.8, '2017': 93.7}, {product: 'Milk Tea', '2015': 83.1, '2016': 73.4, '2017': 55.1}, {product: 'Cheese Cocoa', '2015': 86.4, '2016': 65.2, '2017': 82.5}, {product: 'Walnut Brownie', '2015': 72.4, '2016': 53.9, '2017': 39.1} ]"
            ></mychart>
        </div>
        <div class="ec-box">
            <mychart
            chart-type="line"
            chart-dimensions="['product', '2015', '2016', '2017']"
            chart-dataset-source="[{product: 'Matcha Latte', '2015': 43.3, '2016': 85.8, '2017': 93.7}, {product: 'Milk Tea', '2015': 83.1, '2016': 73.4, '2017': 55.1}, {product: 'Cheese Cocoa', '2015': 86.4, '2016': 65.2, '2017': 82.5}, {product: 'Walnut Brownie', '2015': 72.4, '2016': 53.9, '2017': 39.1} ]"
            ></mychart>
        </div>
        <div class="ec-box">
            <mychart
            chart-type="scatter"
            chart-dimensions="['product', '2015', '2016', '2017']"
            chart-dataset-source="[{product: 'Matcha Latte', '2015': 43.3, '2016': 85.8, '2017': 93.7}, {product: 'Milk Tea', '2015': 83.1, '2016': 73.4, '2017': 55.1}, {product: 'Cheese Cocoa', '2015': 86.4, '2016': 65.2, '2017': 82.5}, {product: 'Walnut Brownie', '2015': 72.4, '2016': 53.9, '2017': 39.1} ]"
            ></mychart>
        </div>
        <div class="ec-box">
            <mychart
            chart-type="funnel"
            chart-dimensions="['product', '2015', '2016', '2017']"
            chart-dataset-source="[{product: 'Matcha Latte', '2015': 43.3, '2016': 85.8, '2017': 93.7}, {product: 'Milk Tea', '2015': 83.1, '2016': 73.4, '2017': 55.1}, {product: 'Cheese Cocoa', '2015': 86.4, '2016': 65.2, '2017': 82.5}, {product: 'Walnut Brownie', '2015': 72.4, '2016': 53.9, '2017': 39.1} ]"
            ></mychart>
        </div>
        <div class="ec-box">
            <mychart
            chart-type="pie"
            chart-dimensions="['product', '2015', '2016', '2017']"
            chart-dataset-source="[{product: 'Matcha Latte', '2015': 43.3, '2016': 85.8, '2017': 93.7}, {product: 'Milk Tea', '2015': 83.1, '2016': 73.4, '2017': 55.1}, {product: 'Cheese Cocoa', '2015': 86.4, '2016': 65.2, '2017': 82.5}, {product: 'Walnut Brownie', '2015': 72.4, '2016': 53.9, '2017': 39.1} ]"
            ></mychart>
        </div>
        <div class="ec-box">
            <mychart
            chart-type="effectScatter"
            chart-dimensions="['product', '2015', '2016', '2017']"
            chart-dataset-source="[{product: 'Matcha Latte', '2015': 43.3, '2016': 85.8, '2017': 93.7}, {product: 'Milk Tea', '2015': 83.1, '2016': 73.4, '2017': 55.1}, {product: 'Cheese Cocoa', '2015': 86.4, '2016': 65.2, '2017': 82.5}, {product: 'Walnut Brownie', '2015': 72.4, '2016': 53.9, '2017': 39.1} ]"
            ></mychart>
        </div>
  </div>
</template>

<script>
import mychart from './components/MyChart.vue'

export default {
  name: 'app',
  components: {
    mychart
  }
}
</script>

<style>
html,body{height:100%;margin:0;padding:0;}
.ec-box{width:33.33%;height:50%;float:left;}
#app {
  height:100%;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
