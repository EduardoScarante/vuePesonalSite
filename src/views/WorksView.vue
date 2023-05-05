<script>

export default {
  data() {
    return {
      index: 0,

      empresaArray: [
        {
          empresa: "JMalucelli",
          funções: "Estagiário",
          description: "Primeiro contato com programação, C++ e Python para montagem de scripts",
          tempo: "1 ano e 4 meses"
        },
        {
          empresa: "Copel",
          funções: "Estágio",
          description: "Primeiros códigos em PHP, usando xampp e mysql",
          tempo: "3 meses"
        },
        {
          empresa: "Just in Time Engenharia",
          funções: "Estágio 'Chefe'",
          description: "Desenvolvimento mobile via React Native e Ionic. Python e JS para script",
          tempo: "2 anos e 2 meses",

        },
        {
          empresa: "Elco Engenharia",
          funções: "Estágio",
          description: "SQL para Oracle, desenvolvimento de relatórios - Power BI, scripts python para automatização de tarefas",
          tempo: "1 ano",

        },
        {
          empresa: "4network",
          funções: "Desenvolvedor",
          description: "Php, postgress, Vue",
          tempo: "6 meses"
        }
      ]
    }
  },
  methods: {
    indexCardMenos() {
      this.index == 0 ? this.index = 0 : this.index--
    },
    indexCardMais() {
      this.index == 4 ? this.index = 4 : this.index++
    }
  },
  computed: {
    infoEmpresa() {
      return this.empresaArray[this.index]
    }
  }
}
</script>


<template>
  <div class="work">

    <div class="cards">
      <button @click="indexCardMenos">&lt</button>
      <div class="card">
        <h1>{{ infoEmpresa.empresa }}</h1>
        <h2>{{ infoEmpresa.funções }}</h2>
        <h3>{{ infoEmpresa.description }}</h3>
        <h4>{{ infoEmpresa.tempo }} meses</h4>
      </div>
      <button @click="indexCardMais">></button>
    </div>

  </div>
</template>

<style scoped>
.work {
  display: flex;
  justify-content: center;
}

.title {
  text-align: center;
}

.cards {
  max-width: 800px;
  padding-top: 80px;

  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.cards button {
  background-color: black;
  color: white;
  font-weight: 800;
  width: 30px;
  height: 30px;
  border-radius: 10px;
  border: none;
  text-decoration: none;
  transition: 0.6s ease-in-out;
}

.cards button:hover {
  background-color: red;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;


  height: 300px;
  width: 400px;

  margin: 10px;
  padding: 25px;

  box-shadow: 3px 3px 3px rgb(7, 7, 7);
  border-radius: 20px;
  background-color: #212121;
  transition: 0.6s ease-in-out;
}

.card:hover {
  box-shadow: 0px 0px 3px rgb(253, 253, 253);
}

h1 {
  font-size: 24px;
  font-weight: 400;

}

h2 {
  font-size: 20px;
  font-weight: 200;

}

h3 {
  font-size: 16px;
  font-weight: 200;

}

h4 {
  font-size: 12px;
  font-weight: 200;
}
</style>
