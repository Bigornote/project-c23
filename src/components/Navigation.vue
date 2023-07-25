<script scoped setup>
import { gsap } from "gsap";
import { onMounted } from "vue";

const nav = [".navbar .title", ".navbar .work"];
onMounted(() => {
  gsap.fromTo(
    nav,
    { opacity: 0, y: 50 },
    { opacity: 1, y: 0, duration: 1, delay: 0.5 }
  );
  gsap.fromTo(
    ".icon-triangle",
    { opacity: 0, y: -20, rotate: -20 },
    { opacity: 1, y: 0, rotate: 0, duration: 1, delay: 0.5 }
  );
});
</script>

<template>
  <section class="navbar">
    <div class="nav">
      <p class="title">Gsap Training</p>
      <img class="icon-triangle" src="../assets/triangle.svg" />
      <p class="work">Selected W0rks</p>
    </div>
    <div class="info">
      <p>G.D<br />Greensock.design</p>
      <p>Design<br />& Art direction</p>
      <p>All Rights Reserved<br />C.23</p>
      <p>France, Fr</p>
    </div>
  </section>
</template>

<style scoped lang="css">
.navbar {
  display: flex;
  flex-direction: column;
  padding: 1vw;
  gap: 1.5vw;
}
.nav {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
}
.title,
.work {
  width: 45%;
  font-size: 5vw;
}
.icon-triangle {
  position: relative;
  top: -1vw;
  width: 20px;
  align-self: flex-end;
}
.info {
  display: flex;
  justify-content: space-between;
}
</style>
