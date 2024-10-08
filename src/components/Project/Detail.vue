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
    <h3>{{ props.subTitle }}</h3>
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
  margin-bottom: 12px;
}

.stack {
  color: black;
  background-color: lightblue;
  margin: 4px 0px;
  padding: 4px 8px;
  border-radius: 48px;
  text-align: center;
}

.button {
  background-color: lightblue;
  padding: 8px;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
    background-color: rgb(80, 177, 209);
}
</style>
