<template>
  <div>
    <span>Details</span>
    <span>+380xxxxxxxxx</span>
    <span>petro.ivankiv88@gmail.com</span>
  </div>
</template>

<script>
export default {
  name: "Details"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
  display: flex;
  flex-direction: column;
  margin-top: 15px;
  font-size: 14px;
  align-items: flex-start;
}

span { line-height: 1.5; }
span:first-of-type { font-weight: bold; }
span:last-of-type { color: blue; }
</style>
