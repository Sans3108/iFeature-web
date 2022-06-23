<script setup>

</script>

<template>
  <div class="wrapper">
    <div class="logo">
      <img src="../assets/logo.png">
    </div>
    <div class="title">
      <span>iFeature - Deutscher Komponist und Künstler</span>
    </div>
  </div>

</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  gap: 10px;
  height: 60px;
  background-color: var(--background-color-soft);
  box-shadow: 0px 3px 15px rgba(0, 0, 0, 0.2);
}

.wrapper:first-child {
  padding-left: 2%;
}

.wrapper:last-child {
  padding-right: 2%;
}

.logo {
  display: flex;
  justify-items: center;
}

.logo>img {
  transition: all .2s ease-in-out;
  transform: scale(0.8);
}

.logo>img:hover {
  transform: scale(0.6);
}

.title {
  position: absolute;
  top: 30px;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  justify-items: center;
  align-items: center;
  font-size: 1.5rem;
}
</style>