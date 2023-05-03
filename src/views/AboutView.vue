<script>

export default {
  data() {
    return {
      index: 1,

      imageSrcAyla:
        [
          "../../src/img/a1.jpeg",
          "../../src/img/a2.jpeg",
          "../../src/img/a3.jpeg",
          "../../src/img/a4.jpeg",
          "../../src/img/n1.jpeg",
          "../../src/img/n2.jpeg",
          "../../src/img/n3.jpeg",
          "../../src/img/n4.jpeg"
        ]
    }
  },
  methods: {
    indexImgMais() {
      this.index == 7 ? this.index = 7 : this.index++
    },
    indexImgMenos() {
      this.index == 0 ? this.index = 0 : this.index--
    },
  },
  computed: {
    urlCat() {
      return this.imageSrcAyla[this.index]
    }

  }
}

</script>

<template>
  <div class="about">
    Sobre mim
    <br>
    Tutor de um casal de catarrentinhos
    <div class="carrosel">
      <button @click="indexImgMenos">&lt</button>
      <img :src='urlCat' alt="" />
      <button @click="indexImgMais">></button>
    </div>



    <div>{{ index }}</div>
    <div>{{ urlCat }}</div>
  </div>
</template>

<style>
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.carrosel{
  display: flex;
  justify-content: center;
}

.carrosel btn{
  text-decoration: none;
}

img {
  height: 300px;
}
</style>
