<template>
  <main class="flex-center">
    <section class="container">
      <ChartBox :surveyData="surveyData" />
      <TabBox :surveyData="surveyData" />
    </section>
  </main>
</template>

<script>
import { surveyData } from "./data";
import ChartBox from "./components/ChartBox.vue";

export default {
  name: "App",
  components: {
    ChartBox,
  },
  data() {
    return {
      surveyData,
    };
  },
  methods: {
    setSearchResult() {},
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

body {
  font-size: 1.6rem;
  font-family: "Noto Sans", sans-serif;
  user-select: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -o-user-select: none;
}

main {
  width: 100vw;
  height: 100vh;
  background-color: #e5e5e5;
}

.container {
  width: 360px;
  height: 785px;
  background-color: #fff;
}

.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
