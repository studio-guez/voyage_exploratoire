<template>
    <header
        class="v-app-header app-rm-user-event"
    >
      <div class="v-app-header__title">Novembre 2024 + Voyage Exploratoire</div>
      <h2>À la découverte de nouvelles façons de faire des lieux à impact social</h2>
    </header>
</template>


<style lang="scss" scoped >
.v-app-header {
  box-sizing: border-box;
  width: 100%;
  position: relative;
  border: solid var(--app-border-width) var(--app-color-beige--dark);
  border-bottom: none;
  align-items: center;
}

.v-app-header__title {
  font-size: 1rem;
  padding-left: var(--app-gutter);
  padding-right: var(--app-gutter);
  font-weight: 700;
  text-transform: uppercase;
  margin-top: 1rem;
}

h2 {
  padding-left: var(--app-gutter);
  padding-right: var(--app-gutter);
  border: none;
  margin-top: .5rem;
  margin-bottom: .5rem;
}

</style>

<script setup lang="ts">
</script>
