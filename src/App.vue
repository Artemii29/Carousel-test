<template>
    <carousel :items="Items" />
</template>

<script>
import Carousel from './components/Carousel.vue';

export default {
  components: {
    Carousel
  },
  data() {
    return {
      Items: [
        { type: 'text', content: 'Пример текста', background: 'grey' },
        { type: 'image', src: 'image.jpg', background: 'green' },
        { type: 'input', placeholder: 'Введите текст', background: 'purple' },
        { type: 'video', src: 'video.mp4', background: 'orangered' }
      ]
    };
  }
};
</script>