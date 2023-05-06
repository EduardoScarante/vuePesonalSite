
<script>
import card from '../components/card.vue';

export default {
  data() {
    return {
      tech:
        [
          {
            path: "./src/img/logoProg/vue.png",
            title: "Vue.js",
            subtitle: "Front End"
          },
          {
            path: "./src/img/logoProg/node.jpg",
            title: "Node.js",
            subtitle: "Back End"
          },
          {
            path: "./src/img/logoProg/python.jpg",
            title: "Python",
            subtitle: "Script / Automatização"
          },
          {
            path: "./src/img/logoProg/sql.webp",
            title: "SQL - Oracle | SQLserver ",
            subtitle: "Data"
          },
          {
            path: "./src/img/logoProg/pb.png",
            title: "Power BI",
            subtitle: "Data Analytics"
          },
          {
            path: "./src/img/logoProg/java.webp",
            title: "Java",
            subtitle: "Back End"
          }
        ]
    }
  },
  components: {
    card
  }
}

</script>

<template>
  <div class="about">
    <div v-for="x in tech">
      <card :data="x.title" :path="x.path" :subtitle="x.subtitle" />
    </div>
  </div>
</template>

<style scoped>
.about {

  width: 600px;
  padding-top: 80px;

  margin: auto;
  place-items: center;
  
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;

  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
