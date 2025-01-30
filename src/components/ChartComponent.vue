<template>
    <div ref="chart" style="width: 100%; height: 400px;"></div>
  </template>
  
  <script lang="ts">
  import { defineComponent, onMounted, ref } from 'vue';
  import * as echarts from 'echarts';
  
  export default defineComponent({
    name: 'ChartComponent',
    setup() {
      const chartRef = ref<HTMLElement | null>(null);
  
      onMounted(() => {
        if (chartRef.value) {
          const myChart = echarts.init(chartRef.value);
          const option = {
            title: {
              text: 'Despesas Mensais',
              left: 'center'
            },
            tooltip: {},
            legend: {
              data: ['Despesas']
            },
            xAxis: {
              data: ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez']
            },
            yAxis: {},
            series: [{
              name: 'Despesas',
              type: 'bar',
              data: [220, 182, 191, 234, 290, 330, 310, 450, 500, 520, 630, 720]
            }]
          };
          myChart.setOption(option);
        }
      });
  
      return {
        chartRef
      };
    }
  });
  </script>
  
  <style scoped>
  div {
    margin: 20px 0;
  }
  </style>
  