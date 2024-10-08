<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
const props = defineProps({
  id: Int16Array,
  title: String,
  subTitle: String,
  role: String,
  frontend: Array,
  backend: Array,
  link: String
})

const onClick = () => {
  if (props.link !== '') {
    window.location.href = props.link
  } else {
    alert('Link not available')
  }
}
</script>

<template>
  <div class="container">
    <h1>{{ props.title }}</h1>
    <h2>{{ props.subTitle }}</h2>
    <h3>{{ props.role }}</h3>
    <div class="full">
      <div>
        Frontend
        <div v-for="item in props.frontend" :key="item.id">
          <div class="stack">{{ item }}</div>
        </div>
      </div>
      <div>
        Backend
        <div v-for="item in props.backend" :key="item.id">
          <div class="stack">{{ item }}</div>
        </div>
      </div>
    </div>
    <div>
      <button class="button" @click="onClick">Source code</button>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.full {
  display: flex;
  gap: 48px;
}

.stack {
  color: black;
  margin: 4px 0px;
  padding: 4px 8px;
  background-color: lightblue;
  border-radius: 48px;
  text-align: center;
}

.button {
  padding: 4px;
  border-radius: 4px;
  background-color: lightblue;
}
</style>
