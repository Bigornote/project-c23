<script setup></script>

<template>
  <section class="modal">
    <div class="modal-nav">
      <div class="btn-close">
        <button @click="">close</button>
      </div>
    </div>
    <div class="wrapper">
      <div class="content">
        <p class="number">{{ projectNumber }}</p>
        <p class="title">{{ title }}</p>
      </div>
      <div class="img">
        <img :src="image" alt="{{dataImg}}" />
      </div>
    </div>
  </section>
</template>

<style scoped lang="css">
.modal {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: #fff;
  overflow: hidden;
  scroll-behavior: auto;
}

.modal-nav {
  padding: 1vw;
  display: flex;
  align-items: center;
  justify-content: center;
}

.wrapper {
  display: block;
  display: flex;
  align-items: end;
  height: 90vh;
  padding: 1vw;
  gap: 3vw;
}

.content,
.img {
  width: 50%;
}
.content {
  object-fit: cover;
  text-align: right;
}
.img img {
  object-fit: cover;
  width: 80%;
  height: 80vh;
}
</style>
