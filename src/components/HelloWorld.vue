<script>

import Chart from 'chart.js/auto';

export default {
  data() {
    return {
      setting_model: {}
    };
  },


  mounted() {
    const ctx = document.getElementById('myChart');
    const myChart = new Chart(ctx, {
      type: 'radar',
      data: {
        labels: ['GENERAL', 'ORGANISATION INTERNE', 'RELATION EXTERNE', 'SANTE GLOBAL'],
        datasets: [{
          label: 'RÉSULTATS',
          data: [12, 16, 10, 19],

          backgroundColor: [
            'rgba(10, 50, 255, 0.0)',
            'rgba(10, 50, 245, 0.0)',
            'rgba(10, 50, 245, 0.0)',
            'rgba(10, 50, 255, 0.4)',
          ],
          borderColor: [
            'rgba(68, 114, 196, 1)',
            'rgba(68, 114, 196, 1)',
            'rgba(68, 114, 196, 1)',
            'rgba(68, 114, 196, 1)',
          ],

          borderWidth: 3
        }]
      },
      options: {
        elements: {
          line: {
            borderWidth: 4
          }
        }
      }
    });
    myChart
  },

};
</script>

<template>
  <div class="greetings">
    <div class="bg-white square">
      <canvas id="myChart" class="myChart" style="width: 705px;height: 573px;"></canvas>
    </div>
  </div>
</template>

<style scoped>
.square {
    width: 800px;
    height: 699px;
    display: flex;
    align-items: center;
    justify-content: center;
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {

  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
