<script setup lang="ts">
import Card from "./Card.vue";
</script>

<template>
  <section class="galery">
    <div class="top-content">
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
    </div>

    <div class="bottom-content">
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
      <Card
        projectNumber="P.001"
        title="Hello"
        image="/src/assets/little-project.png"
        dataImg="Test d'un image"
      />
    </div>

    <div class="number-content">
      <p>C.23</p>
    </div>
  </section>
</template>

<style lang="css">
.galery {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 8vw;
  padding: 1vw;
}
.top-content {
  display: flex;
  justify-content: space-between;
}

.top-content .card:nth-child(2) {
  transform: translateX(-4vw);
}

.top-content .card:nth-child(3) {
  transform: translateX(4vw);
}

.bottom-content {
  display: flex;
  justify-content: space-around;
}

.bottom-content .card:nth-child(2) {
  transform: translateX(6vw);
}

.number-content {
  position: absolute;
  bottom: 10vh;
  right: 20vw;
  font-size: 50px;
}
</style>
