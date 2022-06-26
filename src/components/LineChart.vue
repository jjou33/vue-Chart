<template>
  <div>
    <canvas ref="myLineChart"></canvas>
  </div>
</template>

<script>
import { Chart, registerables } from "chart.js";

Chart.register(...registerables);

export default {
  mounted() {
    const labels = ["January", "February", "March", "April", "May", "June"];

    const data = {
      labels: labels,
      datasets: [
        {
          label: "My First dataset",
          backgroundColor: "rgb(255, 99, 132)",
          borderColor: "rgb(255, 99, 132)",
          data: [0, 10, 5, 2, 20, 30, 45],
        },
      ],
    };

    const config = {
      type: "line",
      data: data,
      options: {},
    };
    const myLineChart = new Chart(this.$refs.myLineChart, config);
  },
};
</script>

<style></style>
