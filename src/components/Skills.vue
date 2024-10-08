<!-- eslint-disable vue/multi-word-component-names -->
<script></script>

<template>
  <div class="card">
    <div class="title">
      <h1>SKILLS</h1>
    </div>
    <div class="content">
      <div class="program">
        <div>
          <h2>Programming</h2>
        </div>
        <div class="program-icon">
          <div>
            <img src="../assets/icons/C.svg" alt="C" />
            <p>C</p>
          </div>
          <div>
            <img src="../assets/icons/Python.svg" alt="" />
            <p>Python</p>
          </div>
        </div>
      </div>
      <div class="web">
        <div>
          <h2>Web Development</h2>
        </div>
        <div class="web-icon">
          <div>
            <img src="../assets/icons/HTML.svg" alt="" />
            <p>HTML</p>
          </div>
          <div>
            <img src="../assets/icons/CSS.svg" alt="" />
            <p>CSS / Tailwind</p>
          </div>
          <div>
            <img src="../assets/icons/JSTS.svg" alt="" />
            <p>Javascript / Typescript</p>
          </div>
          <div>
            <img src="../assets/icons/React.svg" alt="" />
            <p>React</p>
          </div>
          <div>
            <img src="../assets/icons/Vue.svg" alt="" />
            <p>Vue</p>
          </div>
          <div>
            <img src="../assets/icons/NodeJS.svg" alt="" />
            <p>NodeJS</p>
          </div>
        </div>
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

.title {
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

.program {
  text-align: center;
}

.program-icon {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  /* display: flex;
  flex-direction: column; */
  gap: 12px;
}

.web {
  text-align: center;
}

.web-icon {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.web-icon .div {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

img {
  width: 120px;
  margin: 16px 0px;
}
</style>
