<script>
import card from "../components/card.vue";

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
          path: Vue,
          title: "Vue JS",
          subtitle: "Front End",
        },
        {
          path: Node,
          title: "Node JS",
          subtitle: "Back End",
        },
        {
          path: Python,
          title: "Python",
          subtitle: "Script / Automatização",
        },
        {
          path: SQL,
          title: "SQL",
          subtitle: "Análises de Dados",
        },
        {
          path: Power,
          title: "Power BI",
          subtitle: "Data Analytics",
        },
        {
          path: Java,
          title: "Java",
          subtitle: "Back End",
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

  <div class="chart">
    <span>Vue JS</span>
    <footer>
      <div data-width="95%" style="width: 95%"></div>
    </footer>
  </div>

  <div class="chart">
    <span>Node JS</span>
    <footer>
      <div data-width="95%" style="width: 95%"></div>
    </footer>
  </div>

  <div class="chart">
    <span>Python</span>
    <footer>
      <div data-width="95%" style="width: 95%"></div>
    </footer>
  </div>

  <div class="chart">
    <span>SQL</span>
    <footer>
      <div data-width="95%" style="width: 95%"></div>
    </footer>
  </div>

  <div class="chart">
    <span>Power BI</span>
    <footer>
      <div data-width="95%" style="width: 95%"></div>
    </footer>
  </div>

  <div class="chart">
    <span>Java</span>
    <footer>
      <div data-width="95%" style="width: 95%"></div>
    </footer>
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

.chart {
  margin: 3rem 25em 2rem 25rem;
}

.chart span {
  font-size: 18px;
  margin-bottom: 7px;
  display: block;
}

.chart footer {
  background-color: rgb(215, 245, 250);
  height: 2px;
}

.chart footer div {
  height: 100%;
  background-color: aqua;
  transition: width 1.3s ease-out;
}
</style>
