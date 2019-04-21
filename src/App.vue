<template>
  <div id="app">
    <Header name="Petro Ivankiv" position="Front End Developer"/>
    <div class="content">
      <section>
        <CvSection title="Profile" icon="profile.svg" :items="profileItems"/>
      </section>
      <aside>this is an aside</aside>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import CvSection from "./components/CvSection.vue";

export default {
  name: "app",
  components: {
    Header,
    CvSection
  },
  computed: {
    profileItems: function() {
      return [
        {
          id: 1,
          description:
            "Passionated front end developer with 2+ year of experiance. " + 
            "Self-motivated, sensible, sosiable, a good team player"
        }
      ];
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px;
}

.content {
  display: flex;
  margin: 35px 0;
}
section {
  width: 70%;
}
aside {
  width: 30%;
}
</style>
