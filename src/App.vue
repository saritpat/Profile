<script setup>
import Intro from './components/Intro.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Experience from './components/Experience.vue'
</script>

<template>
  <div class="container">
    <div class="section">
      <Intro />
    </div>
    <div class="section">
      <Skills />
    </div>
    <div class="section">
      <Projects />
    </div>
    <div class="section">
      <Experience />
    </div>
  </div>
</template>

<style scoped>
.container {
  /* lightblue #6FB7FA */
  background-color: #004caf;
}

.section {
  padding: 10px 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>

<!-- <script>
export default {
  data() {
    return {
      name:"Saritpat",
      status: 'active',
      tasks: [
        't1','t2','t3'
      ],
      link: 'https://google.com'
    }
  },
  methods: {
    onClick() {
      if (this.status === 'active') {
        this.status = 'pending'
      } else if (this.status === 'pending') {
        this.status = 'inactive'
      } else {
        this.status = 'active'
      }
    }
  }
}
</script>
<template>
  <h1>{{name}}</h1>
  <p v-if="status === 'active'">User active</p>
  <p v-else-if="status === 'pending'">User pending</p>
  <p v-else>User inactive</p>

  <p>task</p>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <a :href="link">google</a>

  <button @click="onClick">Change status</button>
</template>

<style scoped>

</style> -->
