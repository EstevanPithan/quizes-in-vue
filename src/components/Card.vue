<script setup lang="ts">
import { defineProps } from "vue"

const { quiz } = defineProps(['quiz'])
</script>


<template>
  <div class="card">
    <img :src="quiz.img" alt="">
    <div class="card-text">
      <h2>{{ quiz.name }}</h2>
      <p>{{ quiz.questions.length }} questions</p>
    </div>
  </div>
</template>


<style scoped>
.card {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  border-radius: 8px;
  padding: 4px 8px;
  margin: 4px 8px;
  cursor: pointer;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.1);
}

.card:hover {
  transform: scale(1.01);
  opacity: 0.6;
}

.card img {
  width: 300px;
}

.card-text {
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
  flex-direction: column;
  width: 100%;
  margin: 4px;
}

.card-text p {
  color: gray;

}
</style>