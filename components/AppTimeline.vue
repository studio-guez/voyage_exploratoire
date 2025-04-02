<template>
    <section class="v-app-timeline"
    >
      <template v-for="item of items">
        <div class="v-app-timeline__item">
          <div class="v-app-timeline__item__circle"></div>
          <div>
            <div class="v-app-timeline__item__title app-font-h3">{{item.title}}</div>
            <div class="v-app-timeline__item__date app-font-h4">{{item.date}}</div>
            <div class="v-app-timeline__item__description app-font-p">{{item.description}}</div>
          </div>
        </div>
      </template>
    </section>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

defineProps<{
    items: {
        title: string,
        description: string,
        date: string,
    }[]
}>()
</script>





<style lang="scss" scoped >
.v-app-timeline__item {
  display: flex;
  align-items: flex-start;
  gap: var(--app-gutter);
  margin-bottom: 1rem;
}

.v-app-timeline__item__circle {
  display: block;
  border: solid 1px var(--app-color-beige--dark);
  border-radius: 4rem;
  width: 2rem;
  height: 2rem;
}

.v-app-timeline__item__date {
  color: var(--app-color-beige--dark);
}

.v-app-timeline__item__description {
  color: var(--app-color-beige--dark);
}

</style>
