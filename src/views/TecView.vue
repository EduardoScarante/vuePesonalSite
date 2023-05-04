
<script>
import card from '../components/card.vue';

export default {
  data() {
    return {
      tech:
        [
          {
            path: "../../src/img/logoProg/python.jpg",
            title: "Python"
          },
          {
            path: "../../src/img/logoProg/vue.png",
            title: "Vue.js"
          },
          {
            path: "../../src/img/logoProg/node.jpg",
            title: "Node.js"
          },
          {
            path: "../../src/img/logoProg/java.png",
            title: "Java"
          },
          {
            path: "../../src/img/logoProg/sql.webp",
            title: "SQL - oracle | sqlserver"
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
      <card :data="x.title" :path="x.path"/>
    </div>

    <!--     {{ tech }}
 -->
  </div>
</template>

<style scoped>
.about {
  width: 600px;

  padding-top: 100px;
  
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;

  justify-content: center;
  align-items: center;
  text-align: center;
}

</style>
