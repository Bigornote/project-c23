<script setup>
import { gsap } from "gsap";
import { onMounted } from "vue";

const nav = [".navbar .title div span", ".navbar .work div span"];
onMounted(() => {
  gsap.from(nav, 1.2, {
    y: "100%",
    ease: "power4.out",
    delay: 0.5,
    skewY: 7,
    stagger: {
      amount: 0.233,
    },
  });

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
      <div class="title">
        <div><span>Gsap</span></div>
        <div><span>Training</span></div>
      </div>
      <img class="icon-triangle" src="../assets/triangle.svg" />
      <div class="work">
        <div><span>Selected</span></div>
        <div><span>W0rks</span></div>
      </div>
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
}

.title div,
.work div {
  width: 100%;
  height: 5.1vw;
  position: relative;
  overflow: hidden;
}

.title div span,
.work div span {
  position: absolute;
  top: 0;
  left: 50%;
  font-size: 5vw;
  transform: translateX(-50%);
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
