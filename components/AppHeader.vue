<template>
    <header
        class="v-app-header app-rm-user-event"
    >
      <div class="v-app-header__title">Novembre 2024</div>
    </header>
</template>


<style lang="scss" scoped >
.v-app-header {
  box-sizing: border-box;
  width: 100%;
  position: relative;
  border: solid var(--app-border-width) var(--app-color-beige--dark);
  border-bottom: none;
  display: flex;
  height: 2rem;
  align-items: center;
}

.v-app-header__title {
  font-size: 1rem;
  padding-left: var(--app-gutter);
  padding-right: var(--app-gutter);
  font-weight: 700;
  text-transform: uppercase;
}
</style>
