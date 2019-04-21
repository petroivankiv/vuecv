<template>
  <header>
    <div class="header-top">
      <img :src="getIcon()" alt="Icon">
      <span class="title">{{ title }}</span>
    </div>
    <div v-for="item in items" :key="item.id">
      <CvSectionItem :title="item.title" :timeDesc="item.timeDesc" :description="item.description"/>
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
  margin-top: 15px;
}

.header-top {
  display: flex;
  align-items: center;
}

.title {
  font-size: 18px;
  font-weight: bold;
  margin-left: 15px;
}
</style>
