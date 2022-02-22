<template>
  <div class="chart">
    <div class="thumb">
      <img src="../assets/cat.png" alt="cat image" />
    </div>

    <RadarChar :surveyData="surveyData" />
  </div>
</template>

<script>
import RadarChar from "./RadarChar.vue";

export default {
  props: {
    surveyData: Object,
  },
  components: {
    RadarChar,
  },
};
</script>

<style>
.chart {
  width: 360px;
  height: 381px;
  position: relative;
}

.chart .thumb {
  width: 54px;
  height: 54px;
  border-radius: 160px;
  overflow: hidden;
  position: absolute;
  left: 42.22%;
  right: 42.78%;
  top: 43.57%;
  bottom: 42.26%;
  background-color: white;
}

.chart .thumb > img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
