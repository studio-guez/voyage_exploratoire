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
        <svg class="v-app-section__header__icon"
             width="391" height="391" viewBox="0 0 391 391" fill="none" xmlns="http://www.w3.org/2000/svg">
          <g clip-path="url(#clip0_85_194)">
            <path d="M331.567 342.459C280.492 303.154 238.268 325.463 239.772 390.558C215.185 331.302 167.196 329.228 135.982 386.612C144.125 323.366 103.978 297.683 48.095 331.563C87.4 280.491 65.098 238.268 0 239.772C59.256 215.181 61.332 167.196 3.90701 136.628C67.191 144.125 92.874 103.977 58.954 48.741C110.07 87.4 152.29 65.094 150.786 0C175.373 59.256 223.365 61.329 253.927 3.908C246.399 67.838 286.583 92.871 341.813 58.954C303.158 110.066 325.464 152.287 390.558 150.782C331.305 175.373 329.229 223.362 386.616 254.573C322.72 246.396 297.037 286.542 331.567 342.459Z" fill="#AD936E"/>
          </g>
          <defs>
            <clipPath id="clip0_85_194">
              <rect width="390.558" height="390.558" fill="white"/>
            </clipPath>
          </defs>
        </svg>
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
    transform_translate_x: string,
    transform_translate_y: string,
    transform_scale: string,
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
  overflow: hidden;
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
  display: block;
  position: absolute;
  top: 50%;
  right: 0;
  transform:
      translate( v-bind(transform_translate_x) , v-bind(transform_translate_y) )
      scale( v-bind(transform_scale) )
  ;
  height: 100%;
  width: auto;
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
