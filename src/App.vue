<script setup lang="ts">

</script>

<template>
  <div class="container">
    <header>
      <h1>
        QUIZES
      </h1>
      <input type="text" placeholder="Type here to search your Quiz" />
    </header>

    <div class="options-container">

      <div class="card">
        <img src="./assets/img/math.jpg" alt="">
        <div class="card-text">
          <h2>Math</h2>
          <p>15 Questions </p>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped>
.container {
  /* background-color: blue; */
  width: 100vw;
  height: 100vh;

  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  flex-direction: column;
}

header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
  padding: 1rem;
}

header input {
  width: 20%;
  padding: 0.4rem;
  border-radius: 8px;
  border: 1px solid gray;
  margin-left: 1rem;
}

.options-container {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 100%;
  padding: 1rem;
  flex-wrap: wrap;
}

.card {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  border-radius: 8px;
  padding: 4px 8px;
  margin: 4px 8px;
  border: 1px solid black;
  cursor: pointer;
}

.card:hover {
  transform: scale(1.01);
  opacity: 0.6;
}

.card img {
  width: 300px;
  height: 300px;
}
</style>
