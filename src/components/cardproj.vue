<script>
export default {
  props: {
    data: String,
    path: String,
    subtitle: String,
  },
};
</script>

<template>
  <div class="card">
    <div class="title">
      <div class="data">
        {{ data }}
      </div>
      <div class="des">
        {{ subtitle }}
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;

  height: 200px;
  width: 300px;

  margin: 10px;
  padding: 25px;

  box-shadow: 3px 3px 3px rgb(7, 7, 7);
  border-radius: 20px;
  background-color: rgba(0, 0, 0, 0.2);
  transition: 0.6s ease-in-out;
}

.card:hover {
  box-shadow: 0px 0px 3px rgb(255, 255, 255);
}

.data {
  font-weight: 800;
  padding-top: 10px;
}
.des {
  font-weight: 400;
}
</style>
