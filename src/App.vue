<script setup>
import { ref } from 'vue'
import AppCard from './components/AppCard.vue'

const cardsData = ref([
  {
    imgSrc: '/area.jpg',
  },
  {
    imgSrc: '/panorama.jpg',
  },
  {
    imgSrc: '',
  },
  {
    imgSrc: '/road.jpg',
  },
])
</script>

<template>
  <div class="cards container">
    <app-card v-for="(card, index) in cardsData" :img-src-new="card.imgSrc" :key="index">
      <div v-if="!card.imgSrc" class="card">
        <div class="text-wr">
          <p>HTML ㅤㅤㅤCSS</p>
          <p>SPA ㅤㅤㅤREST</p>
          <p>AXIOS ㅤㅤㅤJSON</p>
          <p>NPM ㅤㅤㅤBEM</p>
        </div>
      </div>
    </app-card>
  </div>

  <div class="cards container">
    <div class="card">
      <img class="card-img" src="/area.jpg" alt="picture" />
    </div>
    <div class="card">
      <img class="card-img" src="/panorama.jpg" alt="picture" />
    </div>
    <div class="card">
      <div class="text-wr">
        <p>HTML ㅤㅤㅤCSS</p>
        <p>SPA ㅤㅤㅤREST</p>
        <p>AXIOS ㅤㅤㅤJSON</p>
        <p>NPM ㅤㅤㅤBEM</p>
      </div>
    </div>
    <div class="card">
      <img class="card-img" src="/road.jpg" alt="picture" />
    </div>
  </div>
</template>

<style scoped>
.cards {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 20px;

  padding-top: 20px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.card {
  height: 300px;
  width: 200px;
  border: 1px solid black;
  border-radius: 10px;
  box-shadow: 3px 3px 20px rgba(50, 50, 50, 0.25);
  overflow: hidden;
}

.card-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.text-wr {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
</style>
