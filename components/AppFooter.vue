<template>
    <footer class="v-app-footer app-child-rm-horizontal-margins"
    >
      <p>S'abonner à la newsletter :</p>
      <input type="text" placeholder="adresse mail"/>
      <p>Nous contacter :
        <br>super@lesfantastiquescommuns.cc
        <br>
        <br>L'association les fantastiques communs
        <br>route de la Galaise 23A, 1228 Plan-les-Ouates
      </p>
    </footer>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps<{
    message?: string
}>()
</script>





<style lang="scss" scoped >
.v-app-footer {
  box-sizing: border-box;
  padding: var(--app-gutter);
  color: white;
  background: var(--app-color-beige--dark);
}

input {
  background: transparent;
  border: solid 1px currentColor;
  color: inherit;
  display: block;
  box-sizing: border-box;
  font-size: .75rem;
  line-height: 1.25em;
  padding: 1em;
  width: 100%;
  border-radius: 2em;

  &::placeholder {
    color: inherit;
    text-transform: uppercase;
  }
}

</style>
