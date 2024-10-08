<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import Detail from './Detail.vue'
const props = defineProps({
  id: Int16Array,
  imageName: String,
  title: String,
  subTitle: String,
  role: String,
  frontend: Array,
  backend: Array,
  link: String
})
</script>

<template>
  <div class="block">
    <img :src="imageName" :alt="title" />
    <h1>{{ props.title }}</h1>
    <div class="detail">
      {{ props.data }}
      <Detail
        :title="props.title"
        :subTitle="props.subTitle"
        :role="props.role"
        :frontend="props.frontend"
        :backend="props.backend"
        :link="props.link"
      />
    </div>
  </div>
</template>

<style scoped>
.block {
  display: flex;
  justify-content: center;
  align-items: center;
}

img {
  width: 360px;
  height: 360px;
  transition: filter 0.3s ease;
}

.block:hover img {
  filter: brightness(50%); /* Darken the image by reducing brightness */
}

h1 {
  position: absolute;
}

.block:hover h1 {
  display: none;
}

.detail {
  position: absolute;
  display: none;
}

.block:hover .detail {
  display: block;
  transition: ease;
}
</style>
