<script setup>
const props = defineProps({
  imgSrcNew: {
    type: String,
    required: false,
  },
})
</script>

<template>
  <slot>
    <div v-if="imgSrcNew" class="card">
      <img class="card-img" :src="imgSrcNew" alt="picture" />
      <div class="">{{ imgSrcNew }}</div>
    </div>
  </slot>
</template>

<style scoped>
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
</style>
