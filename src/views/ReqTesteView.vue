<script>
import card from "../components/cardproj.vue";

import Vue from "@/img/logoProg/vue.png";
import Node from "@/img/logoProg/node.jpg";
import Python from "@/img/logoProg/python.jpg";
import SQL from "@/img/logoProg/sql.webp";
import Power from "@/img/logoProg/pb.png";
import Java from "@/img/logoProg/java.webp";

export default {
  data() {
    return {
      tech: [
        {
          // path: Vue,
          title: "Projeto",
          subtitle: "1",
        },
        {
          // path: Node,
          title: "Projeto",
          subtitle: "2",
        },
        {
          // path: Python,
          title: "Projeto",
          subtitle: "3",
        },
        {
          // path: SQL,
          title: "Projeto",
          subtitle: "4",
        },
        {
          // path: Power,
          title: "Projeto",
          subtitle: "5",
        },
        {
          // path: Java,
          title: "Projeto",
          subtitle: "6",
        },
      ],
    };
  },
  components: {
    card,
  },
};
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

<!-- <script>

export default {
  data() {
    return {
      res:
        []
    }
  },
  mounted() {
    fetch("http://127.0.0.1:8000/api/users/",
      {
        method: "GET",
      }
    ).then(res => {
      return res.json()
    }).then(res => {
      this.res = res
    }).catch(err => {
      alert("Algo deu errado, tente mais tarde")
    })
  },


  *(comentado originalmente)  unmounted() {
      console.log("desmontou");
    }, *


  methods: {
    click() {
      console.log("fetch Post fictício");
    }
  }
}

</script>

<template>
  <body>
    <table>
      <tr>
        <td class="c">Nome</td>
        <td class="c">Cor Favorita</td>
        <td class="c">Endereço</td>
        <td class="c">Email</td>
        <td class="c">Nome do Pet</td>
      </tr>

      <tr v-for='x in res'>
        <td>{{ x.name }}</td>
        <td>{{ x.favorite_color }}</td>
        <td>{{ x.address }}</td>
        <td>{{ x.email }}</td>
        <td>{{ x.pet_name }}</td>
      </tr>

    </table>

    *comentado originalmente  <button @click="click">POST</button>  *
 
  </body>
</template>

<style scoped>
body {
  display: flex;
  flex-direction: column;
  height: 80vh;
  justify-content: center;
  text-align: center;
  align-items: center;
}

td {
  font-weight: 400;
  width: 150px;
  text-align: left;

}

table{
  border: 1px solid gray;
}

.c {
  text-align: center;
  font-weight: 800;
  border-bottom: 1px solid gray;J
}
</style> -->
