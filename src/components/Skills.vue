<template>
  <div>
    <span>Skills</span>
    <span>Javascript</span>
    <span>CSS3</span>
    <span>HTML5</span>
    <span>Typescript</span>
    <span>MongoDB</span>
    <span>NODEJS</span>
    <span>Angular 6</span>
    <span>React</span>
    <span>Vue</span>
    <span>Redux</span>
    <span>NGRX</span>
    <span>Git</span>
    <span>Bitbucket</span>
    <span>Git Lab</span>
    <span>Git Lab CI</span>
    <span>Travise</span>
  </div>
</template>

<script>
export default {
  name: "Skills"
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
</style>
