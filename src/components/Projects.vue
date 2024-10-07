<script setup>
import { ref } from 'vue'
import Project from './Project.vue'
const projects = ref([
  {
    id: 1,
    title: 'Blog Blog',
    imageName: new URL('@/assets/images/Blog.png', import.meta.url).href, // Use new URL with import.meta.url
    data: ''
  },
  {
    id: 2,
    title: 'Dorm management system',
    imageName: new URL('@/assets/images/Dorm.png', import.meta.url).href,
    data: ''
  },
  {
    id: 3,
    title: 'Life@KMITL',
    imageName: new URL('@/assets/images/Life.png', import.meta.url).href,
    data: ''
  },
  {
    id: 4,
    title: 'EZcom',
    imageName: new URL('@/assets/images/Ezcom.png', import.meta.url).href,
    data: ''
  }
])
</script>

<template>
  <div class="card">
    <div class="title">
      <h1>PROJECTS</h1>
    </div>
    <div class="content">
      <Project
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :imageName="project.imageName"
        :data="project.data"
      />
    </div>
  </div>
</template>

<style scoped>
* {
  font-family: 'Gill Sans', 'Gill Sans MT', sans-serif;
  color: white;
}

.card {
  width: 66.7%;
  height: 100vh;
  margin: 20px 0;
  padding: 40px;
  background-color: rgb(86, 86, 141);
  border-radius: 28px;
}

.title {
  margin: 16px 4px;
  padding: 28px;
  display: flex;
  justify-content: center;
}

.content {
  display: grid;
  grid-template-columns: repeat(2, 360px);
  gap: 28px;
  justify-content: center;
}
</style>
