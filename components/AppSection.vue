<template>
    <section class="v-app-section"
             ref="appSectionElement"
    >
      <div class="v-app-section__header"
           v-if="title"
      >
          <h2 class="v-app-section__header__title"
          >{{title}}</h2>
        <h3 v-if="subtitle"
            class="v-app-section__header__subtitle">{{subtitle}}</h3>
        <video class="app-display-block v-app-section__header__icon"
               v-if="svg_path"
               :src="svg_path"
               muted
               autoplay
               playsinline
               loop
             />
      </div>
      <div class="v-app-section__body"
           ref="bodyContainer"
      >
        <div class="v-app-section__body__content app-child-rm-horizontal-margins"
             ref="bodyContent"
        >
          <slot/>
        </div>
      </div>
    </section>
</template>





<script setup lang="ts">
import {defineProps, type Ref, type UnwrapRef} from 'vue'

const appSectionElement: Ref<UnwrapRef<null> | HTMLElement> = ref(null)
const bodyContainer: Ref<UnwrapRef<null> | HTMLElement> = ref(null)
const bodyContent: Ref<UnwrapRef<null> | HTMLElement> = ref(null)

defineProps<{
    title?: string
    subtitle?: string
    svg_path?: string
}>()
</script>





<style lang="scss" scoped >
.v-app-section {
  box-sizing: border-box;
}

.v-app-section__header {
  box-sizing: border-box;
  padding: var(--app-gutter);
  border: solid var(--app-border-width) var(--app-color-beige--dark);
  border-bottom: none;
  position: relative;
  transition: color 0s .25s ease-in-out, background 0s .25s ease-in-out;
}

.v-app-section__header__title {
  margin-top: 0;
  margin-bottom: 0;
}

.v-app-section__header__subtitle {
  margin-top: 2em;
  margin-bottom: 0;
}

.v-app-section__header__icon {
  position: absolute;
  top: 50%;
  right: 0;
  transform: translate(0%, -50%);
  height: 100%;
  mix-blend-mode: darken;
}

.v-app-section__body {
  box-sizing: border-box;
  background: var(--app-color-beige);
  color: var(--app-color-red);
  overflow: hidden;
}

.v-app-section__body__content {
  border: solid var(--app-border-width) var(--app-color-beige--dark);
  border-bottom: none;
  padding: var(--app-gutter);
}

.v-app-section__body__content__intro {
  box-sizing: border-box;
  padding-bottom: var(--app-gutter);
  position: relative;

  &:after {
    content: '';
    position: absolute;
    bottom: 0;
    left: calc(-1* var(--app-gutter));
    height: var(--app-border-width);
    background: var(--app-color-beige--dark);
    width: calc( 100% + ( 2 * var(--app-gutter) ));
  }
}
</style>
