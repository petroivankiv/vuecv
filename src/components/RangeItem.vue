<template>
  <div>
    <span>{{ title }}</span>
    <vue-slider v-model="value" v-bind="getOptions" ref="slider"/>
  </div>
</template>

<script>
import VueSlider from "vue-slider-component";
import "vue-slider-component/theme/antd.css";

export default {
  name: "RangeItem",
  components: {
    VueSlider
  },
  props: {
    value: String,
    title: String
  },
  computed: {
    getOptions: function() {
      return {
        dotSize: 4,
        height: 4,
        direction: "ltr",
        min: 0,
        max: 10,
        interval: 1
      };
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
span {
  line-height: 1.5;
  display: block;
  text-align: start;
}

.vue-slider {
  margin-top: 0;
  margin-bottom: 7px;
}
</style>
