<template>
    <nuxt-link class="v-app-file-link"
       :href="`/documents/${project_directory_name}`"
    >
      <div class="v-app-file-link__img"
           :style="{
              'background-image': `url(/web/${project_directory_name}/image_00000.jpg)`
           }"
      >
        <div class="v-app-file-link__img__icon"/>
      </div>

      <div class="v-app-file-link__content app-child-rm-horizontal-margins">
        <h3>{{title}}</h3>

        <div class="v-app-file-link__description"
             v-html="description"
        />

        <button>accéder</button>
      </div>

    </nuxt-link>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

defineProps<{
    title: string
    description: string
    project_directory_name: string
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
  flex-direction: column;
}

.v-app-file-link__description {
  margin-bottom: 1rem;
}

.v-app-file-link__img {
  background: var(--app-color-red);
  width: 100%;
  aspect-ratio: 5/3;
  flex-grow: 0;
  flex-shrink: 0;
  position: relative;
  background-position: center;
  background-size: cover;
  border-radius: 1rem;
}

.v-app-file-link__img__icon {
  background-repeat: no-repeat;
  width: 2rem;
  height: 2rem;
  background-image: url('/icons/download.svg');
  background-size: contain;
  display: inline-block;
  position: absolute;
  top: var(--app-gutter);
  left: var(--app-gutter);
}

.v-app-file-link__content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 100%;
  box-sizing: border-box;
  padding-left: var(--app-gutter);
  padding-bottom: var(--app-gutter);
  padding-right: var(--app-gutter);

  button {
    margin-left: auto;
  }
}
</style>
