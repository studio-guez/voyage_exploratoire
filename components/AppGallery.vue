<template>
    <section
        class="v-app-gallery"
    >
      <template v-for="n in image_number">
        <img class="v-app-gallery__img"
             :src="`${path_directory}/image_${String(n).padStart(5, '0')}.jpg`"
        >
      </template>
    </section>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

defineProps<{
    path_directory: string
    image_number: number
}>()
</script>





<style lang="scss" scoped >
.v-app-gallery {
  display: flex;
  flex-wrap: nowrap;
  width: 100%;
  overflow: scroll !important;
  gap: var(--app-gutter);
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
}

.v-app-gallery__img {
  display: block;
  height: 50vh;
  scroll-snap-align: start;
}

</style>
