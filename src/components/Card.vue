<script setup>
defineProps({
  title: String,
  projectNumber: String,
  dataImg: String,
  image: String,
});
</script>

<template>
  <div class="card">
    <div class="content">
      <p class="number">{{ projectNumber }}</p>
      <p class="title">{{ title }}</p>
    </div>
    <div class="img">
      <img :src="image" alt="{{dataImg}}" />
    </div>
  </div>
</template>

<style lang="css">
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 1vw;
  width: 10.5vw;
  overflow: hidden;
}

.number,
.title {
  margin: 0;
}

.number {
  font-weight: 600;
}

.img {
  object-fit: cover;
  overflow: hidden;
}

.img img {
  width: 100%;
}
</style>
