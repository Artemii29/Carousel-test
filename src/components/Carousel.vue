<template>
  <div class="carousel">
    <div v-for="(item, index) in items" :key="index" class="carousel-item" :style="{ background: item.background }">
      <p v-if="item.type === 'text'">{{ item.content }}</p>

      <img v-else-if="item.type === 'image'" :src="item.src">

      <input v-else-if="item.type === 'input'" type="text" :placeholder="item.placeholder">

      <video v-else-if="item.type === 'video'" :src="item.src" controls>
        <source >
      </video>
    </div>
  </div>
</template>

<script>
export default {
  props: ['items']
};
</script>

<style>
.carousel {
  aspect-ratio: 2 / 1;
  display: flex;
  overflow-x: auto;
}

.carousel-item {
  flex: 0 0 auto;
  width: 100%;
  height: 100%;
}
</style>
