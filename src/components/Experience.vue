<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import { ref } from 'vue'

const lists = ref([
  {
    id: 1,
    title: 'Santang Corporation CO.,LTD.',
    role: 'Frontend Developer Intern'
  }
])
</script>

<template>
  <div class="card">
    <div class="header">
      <h1>EXPERIENCE</h1>
    </div>
    <div class="content">
      <div class="item" v-for="list in lists" :key="list.id">
        <h2 class="title">
          {{ list.title }}
        </h2>
        {{ list.role }}
      </div>
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

.header {
  margin: 16px 4px;
  padding: 28px;
  display: flex;
  justify-content: center;
}

.content {
  display: flex;
  gap: 200px;
  justify-content: center;
}

.item {
  color: black;
  padding: 28px;
  background-color: rgba(255, 255, 255, 0.35);
  border-radius: 24px;
}

.title {
  color: blue;
}
</style>
