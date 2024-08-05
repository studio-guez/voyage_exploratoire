<template>
    <header
        class="v-app-header app-rm-user-event"
    >
      <video class="v-app-header__video app-display-block"
             src="/shapes/home-rate_5.mp4"
             playsinline
             loop
             muted
             autoplay
      />
      <h1 class="v-app-header__title">Les fantastiques communs</h1>
    </header>
</template>


<style lang="scss" scoped >
.v-app-header {
  box-sizing: border-box;
  width: 100%;
  padding-top: 2rem;
  position: relative;
  box-shadow: inset 0 0 0 1px var(--app-color-beige--dark);
}

.v-app-header__video {
  box-sizing: border-box;
  width: 100%;
  border-radius: 50% 50% 0 0;
  border: solid var(--app-border-width) var(--app-color-beige--dark);
  border-bottom: 0;
}

.v-app-header__title {
  font-size: 1rem;
  padding-left: var(--app-gutter);
  padding-right: var(--app-gutter);
  position: absolute;
  bottom: 0;
  left: 0;
  z-index: 10;
}
</style>
