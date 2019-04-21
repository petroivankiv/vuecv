<template>
  <div class="items-container">
    <span>Skills</span>
    <span v-for="item in items" :key="item.id">
      <RangeItem :value="item.value" :title="item.title"/>
    </span>
  </div>
</template>

<script>
import RangeItem from "./RangeItem.vue";

export default {
  name: "Skills",
  components: {
    RangeItem
  },
  computed: {
    items: function() {
      return [
        { id: "1", value: "9", title: "Javascript" },
        { id: "2", value: "9", title: "CSS3" },
        { id: "3", value: "9", title: "HTML5" },
        { id: "4", value: "9", title: "Typescript" },
        { id: "5", value: "5", title: "MongoDB" },
        { id: "6", value: "6", title: "NODEJS" },
        { id: "7", value: "8", title: "Angular6" },
        { id: "8", value: "6", title: "React" },
        { id: "9", value: "4", title: "Vue" },
        { id: "10", value: "8", title: "Redux" },
        { id: "11", value: "9", title: "NGRX" },
        { id: "12", value: "9", title: "Git" },
        { id: "13", value: "8", title: "Bitbucket" },
        { id: "14", value: "8", title: "GitLab" },
        { id: "15", value: "8", title: "GitLabCI" },
        { id: "16", value: "6", title: "Travise" },
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
