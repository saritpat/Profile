<!-- eslint-disable vue/multi-word-component-names -->
<script></script>

<template>
  <div class="card">
    <div class="intro">
      <div class="text">
        <h2>Hi, I’m Saritpat Niyomthong</h2>
        <h1>Software Developer</h1>
        <p>
          I recently graduated from KMITL and currently looking for a part or full time job to apply
          knowledge and acquire opportunity to develop skills and experience in real world company.
        </p>
      </div>
      <div class="profile">
        <img src="../assets/images/me cool.jpg" alt="me cool" class="profile_img" />
      </div>
    </div>
    <div class="title">
      <h1>EDUCATION</h1>
    </div>
    <div></div>
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
  padding: 40px;
  background-color: rgba(255, 255, 255, 0.35);
  border: 1px solid white;
  border-radius: 28px;
}

.intro {
  display: flex;
  align-items: center;
}

.intro div {
  text-align: center;
}

.intro p {
  margin: 52px 42px 0 52px;
}

.profile_img {
  width: 302px;
  height: 302px;
  border-radius: 100%;
}

.title {
  padding: 28px;
  display: flex;
  justify-content: center;
}
</style>
