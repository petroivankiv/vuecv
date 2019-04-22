<template>
  <section>
    <span v-if="title" class="title">{{ title }}</span>
    <span v-if="timeDesc" class="time-desc">{{ timeDesc }}</span>
    <p v-if="description">{{ description }}</p>
  </section>
</template>

<script>
export default {
  name: "CvSectionItem",
  props: {
    title: String,
    timeDesc: String,
    description: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
section {
  display: flex;
  flex-direction: column;
  margin-left: 38px; 
  padding: 10px 0 5px;
}
.title {
  font-size: 14px;
  font-weight: bold;
}

p { font-size: 14px; }

.time-desc { color: grey; font-size: 12px; }
</style>
