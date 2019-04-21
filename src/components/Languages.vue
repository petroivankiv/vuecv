<template>
  <div class="items-container">
    <span>Languages</span>
    <span v-for="item in items" :key="item.id">
      <RangeItem :value="item.value" :title="item.title"/>
    </span>
  </div>
</template>

<script>
import RangeItem from "./RangeItem.vue";

export default {
  name: "Languages",
  components: {
    RangeItem
  },
  computed: {
    items: function() {
      return [
        { id: "1", value: "10", title: "Ukraine" },
        { id: "2", value: "7", title: "English" },
        { id: "3", value: "8", title: "Russia" }
      ];
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.items-container {
  margin-top: 15px;
  font-size: 14px;
}

span {
  line-height: 1.5;
  display: block;
  text-align: start;
}

span:first-of-type {
  font-weight: bold;
}
</style>
