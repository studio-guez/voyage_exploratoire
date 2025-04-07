<template>
    <section class="v-app-timeline"
    >
      <template v-for="item of items">
        <div class="v-app-timeline__item">
          <div class="v-app-timeline__item__line"></div>
          <div class="v-app-timeline__item__circle"></div>
          <div>
            <div class="v-app-timeline__item__title app-font-h3">{{item.title}}</div>
            <div class="v-app-timeline__item__date app-font-h4">{{item.date}}</div>
            <div class="v-app-timeline__item__subtitle app-font-p">{{item.subtitle}}</div>
            <div class="v-app-timeline__item__description"
                 v-if="item.description"
                 v-html="item.description"
            />
          </div>
        </div>
      </template>
    </section>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'
import {describe} from "node:test";

defineProps<{
    items: {
        title: string,
        description?: string,
        date: string,
        subtitle: string
    }[]
}>()
</script>





<style lang="scss" scoped >
.v-app-timeline {
  overflow: hidden;
}

.v-app-timeline__item {
  display: flex;
  align-items: flex-start;
  gap: var(--app-gutter);
  margin-bottom: 1rem;
  position: relative;
}

.v-app-timeline__item__line {
  display: block;
  position: absolute;
  width: 1px;
  height: 100%;
  background: var(--app-color-beige--dark);
  top: 2rem;
  left: 1rem;
  z-index: 0;
}

.v-app-timeline__item__circle {
  display: block;
  border: solid 1px var(--app-color-beige--dark);
  border-radius: 4rem;
  width: 2rem;
  height: 2rem;
  z-index: 1;
  background: var(--app-color-beige);
  flex-shrink: 0;
}

.v-app-timeline__item__date {
  color: var(--app-color-beige--dark);
}

.v-app-timeline__item__subtitle {
  color: var(--app-color-beige--dark);
}

.v-app-timeline__item__description {

}
</style>
