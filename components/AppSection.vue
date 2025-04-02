<template>
    <section class="v-app-section"
             :class="{
              'is-open': isOpen,
             }"
             @mousedown="onMouseEvent('DOWN')"
             @mouseup="onMouseEvent('UP')"
             @mouseleave="onMouseEvent('LEAVE')"
             @click="onClicked()"
             ref="appSectionElement"
             :id="uniq_id"
    >
      <div class="v-app-section__header app-rm-user-event">
          <h2 class="v-app-section__header__title"
          >{{title}}</h2>
        <h3 v-if="subtitle"
            class="v-app-section__header__subtitle">{{subtitle}}</h3>
        <video class="app-display-block v-app-section__header__icon"
             :src="svg_path"
               muted
               autoplay
               playsinline
               loop
             />
      </div>
      <div class="v-app-section__body app-rm-user-event"
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
const isOpen = ref(false)

const props = defineProps<{
    title: string
    subtitle?: string
    svg_path: string
    uniq_id: string
    is_open?: boolean
}>()

onMounted(() => {nextTick(() => {
    if(props.is_open) {
        isOpen.value = props.is_open
        toggleSection()
    }
})})

function onMouseEvent(direction: 'UP' | 'DOWN' | 'LEAVE') {
    const element = appSectionElement.value
    if( ! (element instanceof HTMLElement)  ) return

    if(direction === 'DOWN') element.classList.add('is-up')
    else element.classList.remove('is-up')
}

function onClicked() {
    isOpen.value = !isOpen.value

    toggleSection()
}

function toggleSection() {
    const containerElement  = bodyContainer.value
    const contentElement    = bodyContent.value

    const contentElementIsReady =
        containerElement instanceof HTMLElement &&
        contentElement instanceof HTMLElement
    if ( ! (contentElementIsReady) ) return

    if(isOpen.value) containerElement.style.height = contentElement.getBoundingClientRect().height + "px"
    else containerElement.style.height = ''
}
</script>





<style lang="scss" scoped >
.v-app-section {
  box-sizing: border-box;
  cursor: pointer;

}

.v-app-section__header {
  box-sizing: border-box;
  padding: var(--app-gutter);
  border: solid var(--app-border-width) var(--app-color-beige--dark);
  border-bottom: none;
  position: relative;
  transition: color 0s .25s ease-in-out, background 0s .25s ease-in-out;

  .is-up & {
    transition: color 0s 0s ease-in-out, background 0s 0s ease-in-out;
    color: var(--app-color-beige);
    background: var(--app-color-red);
  }
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
  transition: height .5s 0s ease-in-out;
  height: 0;
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
