
<script>
import card from '../components/card.vue';

export default {
  data() {
    return {
      tech:
        [
          {
            path: "",
            title: "Python"
          },
          {
            path: "",
            title: "Vue.js"
          },
          {
            path: "",
            title: "React.js"
          },
          {
            path: "",
            title: "Node.js"
          },
          {
            path: "",
            title: "Java"
          },
          {
            path: "",
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
      <card :data="x.title" />
    </div>

    <!--     {{ tech }}
 -->
  </div>
</template>

<style>
.about {
  width: 600px;
  height: 90vh;

  display: flex;
  flex-direction: row;
  flex-wrap: wrap;

  justify-content: center;
  align-items: center;
  text-align: center;
}</style>
