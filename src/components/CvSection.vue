<template>
  <header>
    <img :src="getIcon()" alt="Icon">
    <span class="title">{{ title }}</span>
    <div v-for="item in items" :key="item.id">
      <CvSectionItem :title="item.title" :timeDesc="item.timeDesc" :description="item.description" />
    </div>
  </header>
</template>

<script>
import CvSectionItem from "./CvSectionItem.vue";

export default {
  name: "CvSection",
  components: {
    CvSectionItem
  },
  props: {
    icon: String,
    title: String,
    items: Array
  },
  methods: {
    getIcon() {
      return require("../assets/" + this.icon);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  text-align: left;
}

.title {
  font-size: 24px;
  font-weight: bold;
  margin-left: 15px;
}
</style>
