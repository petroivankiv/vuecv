<template>
  <div id="app">
    <Header name="Petro Ivankiv" position="Front End Developer"/>
    <div class="content">
      <section>
        <CvSection :title="profile.title" :icon="profile.icon" :items="profile.items"/>
        <CvSection :title="history.title" :icon="history.icon" :items="history.items"/>
        <CvSection :title="education.title" :icon="education.icon" :items="education.items"/>
        <CvSection :title="courses.title" :icon="courses.icon" :items="courses.items"/>
        <CvSection
          :title="certifications.title"
          :icon="certifications.icon"
          :items="certifications.items"
        />
      </section>
      <aside>
        <Details/>
        <Links/>
        <Skills/>
        <Languages/>
        <Hobbies/>
      </aside>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import CvSection from "./components/CvSection.vue";
import Details from "./components/Details.vue";
import Links from "./components/Links.vue";
import Skills from "./components/Skills.vue";
import Languages from "./components/Languages.vue";
import Hobbies from "./components/Hobbies.vue";

export default {
  name: "app",
  components: {
    Header,
    CvSection,
    Details,
    Links,
    Skills,
    Languages,
    Hobbies
  },
  computed: {
    profile: function() {
      return {
        icon: "profile.svg",
        title: "Profile",
        items: [
          {
            id: 1,
            description:
              "Passionated front end developer with 3+ year of experiance. " +
              "Self-motivated, sensible, sosiable, a good team player"
          }
        ]
      };
    },
    history: function() {
      return {
        icon: "work-history.svg",
        title: "Employment History",
        items: [
          {
            id: 1,
            title: "Front End Developer at Softserve, Ivano-Frankivsk",
            timeDesc: "November 2016 - Present"
          },
          {
            id: 2,
            title: "Elecrical Engineer at ZPUE Ukraine LLC, Ivano-Frankivsk",
            timeDesc: "October 2013 - November 2016",
            description:
              "Executable function: import of electrical equipment, electric project " +
              "for different construction objects, communication with customers."
          },
          {
            id: 3,
            title: "Elecrical Engineer at Electric Group LLC, Ivano-Frankivsk",
            timeDesc: "June 2011 - October 2013",
            description:
              "Executable function: electric project " +
              "for different construction objects, communication with customers."
          }
        ]
      };
    },
    education: function() {
      return {
        icon: "education.svg",
        title: "Education",
        items: [
          {
            id: 1,
            title: "Master, National University Lviv Polytechnic, Lviv",
            timeDesc: "July 2005 - February 2011"
          },
          {
            id: 2,
            title: "Web Developer, SoftServe IT Academy, Ivano-Frankivsk",
            timeDesc: "July 2005 - February 2011"
          }
        ]
      };
    },
    courses: function() {
      return {
        icon: "courses.svg",
        title: "Courses",
        items: [
          {
            id: 1,
            title: "IT Security Foundation: Core Concepts, LinkedIn",
            timeDesc: "March 2019 - March 2019"
          },
          {
            id: 2,
            title: "NodeJS: Extent and Maintain Aplications, LinkedIn",
            timeDesc: "March 2019 - March 2019"
          },
          {
            id: 3,
            title: "Body Language for Leaders, LinkedIn",
            timeDesc: "February 2019 - February 2019"
          },
          {
            id: 4,
            title: "Concepts of WEB UI Developments, Prometheus",
            timeDesc: "July 2016 - August 2016"
          }
        ]
      };
    },
    certifications: function() {
      return {
        icon: "certifications.svg",
        title: "Certifications",
        items: [
          {
            title: "JS, HTML5, CSS3 - 480, Microsoft",
            timeDesc: "February 2019"
          }
        ]
      };
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
  width: 75%;
}
aside {
  width: 25%;
}
</style>
