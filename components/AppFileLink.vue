<template>
    <a class="v-app-file-link"
       :href="link"
    >
      <div class="v-app-file-link__icon"/>

      <div>
        <h3>{{title}}</h3>

        <div class="v-app-file-link__description"
             v-html="description"
        />

        <button>accéder</button>
      </div>

      <div class="v-app-file-link__img"></div>
    </a>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

defineProps<{
    title: string
    description: string
    link: string
}>()
</script>





<style lang="scss" scoped >
.v-app-file-link {
  color: inherit;
  text-decoration: none;
  display: flex;
  flex-wrap: nowrap;
  gap: var(--app-gutter);
  align-items: flex-start;
  padding-top: 2rem;
  padding-bottom: 2rem;
}

.v-app-file-link__description {
  margin-bottom: 1rem;
}

.v-app-file-link__icon {
  background-repeat: no-repeat;
  width: 2rem;
  height: 2rem;
  background-image: url('/icons/download.svg');
  background-size: contain;
  display: inline-block;
}

.v-app-file-link__img {
  background: var(--app-color-red);
  width: 10rem;
  height: 7rem;
  flex-grow: 0;
  flex-shrink: 0;
}
</style>
