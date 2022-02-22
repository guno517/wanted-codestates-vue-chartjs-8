<script>
import { Radar } from "vue-chartjs";

export default {
  extends: Radar,
  props: {
    surveyData: Object,
  },
  mounted() {
    console.log(this.surveyData);

    this.renderChart(
      {
        labels: [
          ["적극적인", "Aggressive"],
          ["자신있는", "Confident"],
          ["책임있는", "Responsible"],
          ["개인주의", "Indivisual"],
          ["수평적인", "Horizontal"],
        ],
        datasets: [
          {
            label: "My First dataset",
            backgroundColor: "rgba(255, 193, 74, 0.32)",
            borderCapStyle: "round",
            borderColor: "#FFD335",
            pointBackgroundColor: "transparent",
            pointBorderColor: "transparent",
            data: [95, 59, 90, 81, 56],
          },
          {
            label: "My Second dataset",
            backgroundColor: "rgba(110, 60, 249, 0.32)",
            borderCapStyle: "round",
            borderColor: "#6E3CF9",
            pointBackgroundColor: "transparent",
            pointBorderColor: "transparent",
            pointHoverBackgroundColor: "#fff",
            pointHoverBorderColor: "rgba(255,99,132,1)",
            data: [28, 48, 40, 19, 96],
          },
        ],
      },
      { responsive: true, maintainAspectRatio: false, legend: { display: false } }
    );
  },
};
</script>
