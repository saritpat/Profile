<script setup>
const props = defineProps({
  title: String,
  imageName: String,
  data: {
    type: String
  }
})
</script>

<template>
  <div class="block">
    <img :src="imageName" :alt="title" />
    <h1>{{ title }}</h1>
    <div>
      {{ data }}
    </div>
  </div>
</template>

<style scoped>
.block {
  display: flex;
  justify-content: center;
  align-items: center;

  img {
    width: 360px;
    height: 360px;
  }

  h1 {
    position: absolute;
  }
}
</style>
