<script setup>
import Project from './Project.vue'
</script>

<template>
  <div class="card">
    <div class="title">
      <h1>PROJECTS</h1>
    </div>
    <div class="content">
      <Project title="Blog Blog" image="@/assets/images/Blog.png" data="asd" />
      <Project title="Dorm management system" image="@/assets/images/Dorm.png" data="aaa" />
      <Project title="Life@KMITL" :image="'@/assets/images/Life.png'" data="bbb" />
      <Project title="EZcom" :image="'@/assets/images/Ezcom.png'" data="asccd" />
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
