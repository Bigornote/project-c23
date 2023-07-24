<script setup lang="ts"></script>

<template>
  <section class="navbar">
    <div class="top-nav">
      <p class="name">Filip Slovacek</p>
      <p class="icon-triangle">triangle</p>
      <p class="work">Selected Works</p>
    </div>
    <div class="bottom-nav">
      <p>S.D<br />Slovadek.design</p>
      <p>Design<br />& Art direction</p>
      <p>All Rights Reserved<br />C.23</p>
      <p>Prague, CZ</p>
    </div>
  </section>
</template>

<style lang="css">
.navbar {
  display: flex;
  flex-direction: column;
  padding: 10px;
}
.top-nav {
  display: flex;
  justify-content: space-around;
}
.bottom-nav {
  display: flex;
  justify-content: space-between;
}
</style>
