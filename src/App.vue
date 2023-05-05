<script>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/works">Works</RouterLink>
      <RouterLink to="/tec">Technologies</RouterLink>
      <RouterLink to="/about">About Me</RouterLink>
      <RouterLink to="/reqteste">Request - teste</RouterLink>

    </nav>
  </header>

  <RouterView />


  <lottie-player class="lottie" src="../src/img/lotties/bg.json" background="transparent" speed="1" loop autoplay>
  </lottie-player>

</template>



<style scoped>
.lottie {
  position: absolute;
  top: 0px;
  
  background-color: #1D1D1D;

  height: 100vh;
/*   overflow: hidden;
 */
  z-index: -1;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: auto;
}

header {
  line-height: 1.5;

  padding-top: 10px;
  padding-bottom: 10px;
}


nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 0rem;
  font-weight: 200;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
  font-weight: 400;

}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}
</style>
