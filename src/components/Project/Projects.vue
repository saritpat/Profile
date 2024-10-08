<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import { ref } from 'vue'
import Project from './Project.vue'
const projects = ref([
  {
    id: 1,
    imageName: new URL('@/assets/images/Blog.png', import.meta.url).href, // Use new URL with import.meta.url
    title: 'Blog Blog',
    subTitle: 'Blog reading & writing website',
    role: 'Backend developer, 2021',
    frontend: ['HTML', 'CSS', 'JS'],
    backend: ['Django', 'Python'],
    link: ''
  },
  {
    id: 2,
    imageName: new URL('@/assets/images/Dorm.png', import.meta.url).href,
    title: 'Dorm management system',
    subTitle: 'Blog reading & writing website',
    role: 'Frontend developer, 2021',
    frontend: ['HTML', 'CSS', 'JS'],
    backend: ['Django', 'Python'],
    link: 'https://github.com/saritpat/dorm_management'
  },
  {
    id: 3,
    imageName: new URL('@/assets/images/Life.png', import.meta.url).href,
    title: 'Life@KMITL',
    subTitle: 'Blog reading & writing website',
    role: 'Backend developer, 2021',
    frontend: ['HTML', 'CSS', 'JS'],
    backend: ['Django', 'Python'],
    link: 'https://github.com/LifeAtKMITL/dorm-frontend'
  },
  {
    id: 4,
    imageName: new URL('@/assets/images/Ezcom.png', import.meta.url).href,
    title: 'EZcom',
    subTitle: 'Blog reading & writing website',
    role: 'Backend developer, 2021',
    frontend: ['HTML', 'CSS', 'JS'],
    backend: ['Django', 'Python'],
    link: 'https://github.com/ezcom-team/ezcom-client'
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
        :imageName="project.imageName"
        :title="project.title"
        :subTitle="project.subTitle"
        :role="project.role"
        :frontend="project.frontend"
        :backend="project.backend"
        :link="project.link"
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
  background-color: rgba(255, 255, 255, 0.35);
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
