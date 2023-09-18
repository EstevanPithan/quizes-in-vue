<script setup lang="ts">
import { ref, watch } from "vue";
import q from "./data/quizes.json"
import Card from "./components/Card.vue";

const quizes = ref(q)
const search = ref("")
watch(search, () => {
  quizes.value = q.filter(quiz => quiz.name.toLowerCase().includes(search.value))
})

</script>

<template>
  <div class="container">
    <header>
      <h1>
        QUIZES
      </h1>
      <input v-model.trim="search" type="text" placeholder="Type here to search your Quiz" />
    </header>

    <div class="options-container">
      <Card v-for="quiz in quizes" :key="quiz.id" :quiz="quiz" />
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
</style>
