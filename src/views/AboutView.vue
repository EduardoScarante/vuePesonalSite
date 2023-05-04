<script>

import blogCard from '../components/blogCard.vue'

export default {
  components: {
    blogCard
  },
  data() {
    return {
      infos: [
        {
          id: 0,
          nome: "Ayla",
          data: "Preguiçosa, antipática e carente!",
          path: "../../src/img/a1.jpeg"
        },
        {
          id: 1,
          nome: "Nego",
          data: "Brincalhão, cheio de energia e carinhoso!",
          path: "../../src/img/n2.jpeg"
        },
        {
          id: 2,
          nome: "Isa",
          data: "Carinhosa, dorminhoca e otimista!",
          path: "../../src/img/isa.jpeg"
        },
        {
          id: 3,
          nome: "Eduardo",
          data: "Chato, preguiçoso e pessimista",
          path: "../../src/img/edu.png"
        }
      ]
    }
  }
}

</script>

<template>
  <div class="about">

    <div v-for="x in infos">
      <blogCard :nome="infos[x.id].nome" :data="infos[x.id].data" :path="infos[x.id].path" />
    </div>

  </div>
</template>

<style scoped>
.about {
  margin: 50px;
  justify-content: center;

  display: flex;
  flex-wrap: wrap;
  align-items: center;
}
</style>
