<script setup>
import { gsap } from "gsap";
import { onMounted } from "vue";
import Card from "./Card.vue";
import Modal from "./Modal.vue";

onMounted(() => {
  const content = document.querySelectorAll(".card .content");
  const blocImages = document.querySelectorAll(".card .img");

  content.forEach((element, index) => {
    gsap.fromTo(
      element,
      { opacity: 0, skewY: 7 },
      {
        opacity: 1,
        duration: 1,
        skewY: 0,
        ease: "power4.out",
        delay: 1.8 + (index / 2) * 0.2,
      }
    );
  });

  blocImages.forEach((element, index) => {
    if (index % 2 === 0) {
      gsap.fromTo(
        element,
        { opacity: 0, y: -100 },
        {
          opacity: 1,
          y: 0,
          duration: 1.5,
          ease: "power4.inOut",
          delay: 0.8 + (index / 2) * 0.2,
        }
      );
    } else {
      gsap.fromTo(
        element,
        { opacity: 0, y: 100 },
        {
          opacity: 1,
          y: 0,
          duration: 2,
          ease: "power4.inOut",
          delay: 0.8 + ((index - 1) / 2) * 0.5,
        }
      );
    }
  });
});
</script>

<template>
  <section class="galery">
    <div class="top-content">
      <Card
        projectNumber="P.001"
        title="Flow texture"
        image="/src/assets/flow.jpg"
        dataImg="Flow texture polygon"
      />
      <Card
        projectNumber="P.002"
        title="Crystal texture"
        image="/src/assets/crystal.jpg"
        dataImg="Crystal texture"
      />
      <Card
        projectNumber="P.003"
        title="Minimalist interior"
        image="/src/assets/interior.jpg"
        dataImg="Minimalist interior"
      />
      <Card
        projectNumber="P.004"
        title="Unknow resource"
        image="/src/assets/unknow.jpg"
        dataImg="Unknow resource"
      />
    </div>

    <div class="bottom-content">
      <Card
        projectNumber="P.007"
        title="The new hand"
        image="/src/assets/hand.jpg"
        dataImg="Hand texture"
      />

      <Card
        projectNumber="P.006"
        title="IA Revolution"
        image="/src/assets/robot.jpg"
        dataImg="image robot"
      />
      <Card
        projectNumber="P.005"
        title="Bubble texture"
        image="/src/assets/bubble.jpg"
        dataImg="Bubble texture"
      />
    </div>

    <div class="number-content">
      <p>C.23</p>
    </div>
  </section>
  <Modal
    projectNumber="P.001"
    title="Flow texture"
    image="/src/assets/flow.jpg"
    dataImg="Flow texture polygon"
  />
</template>

<style lang="css">
.galery {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 8vw;
  padding: 1vw;
  margin-top: 5vw;
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
  bottom: 1vh;
  right: 20vw;
  font-size: 4vw;
  font-weight: 600;
}
</style>
