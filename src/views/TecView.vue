
<script>
import card from '../components/card.vue';

export default {
  data() {
    return {
      tech:
        [
          "python",
          "vue.js - react.js",
          "js c/ node.js | python | java",
          "sql - oracle | sqlserver"
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
    <card v-for="x in tech"/>
    <card :data=x />
    
    This is an Tecnologias page - View <br>


  </div>

  <componentTeste />
</template>

<style>
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
