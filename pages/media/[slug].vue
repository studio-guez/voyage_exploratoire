<template>
    <section class="v--slug"
    >
      <div class="v--slug__header">
        <h2 class="v--slug__title"
        >Les fantastiques<br>communs</h2>
      </div>
      <div class="v--slug__wrap">
        <template v-if="videoID">
          <video class="v--slug__wrap__video"
                 playsinline
                 controls
                 :src="`https://nextcloud.superhangar.cc/s/${videoID}/download/index.mp4`"
          />
        </template>
        <template v-else>
          <div class="v--slug__wrap__loading-msg">
            récupération de la vidéo :)
          </div>
        </template>
      </div>

      <AppFooter/>
    </section>
</template>





<script setup lang="ts">
import {useRoute} from "vue-router";

const videoID: Ref<string | null> = ref(null)
const videoLoadingHasStart = ref(false)

onMounted(() => {
    const slug = useRoute().params.slug

    if( typeof slug  === 'string')
        window.setTimeout(() => videoID.value = slug, 2_000)
})

</script>





<style lang="scss" scoped >
.v--slug {
  box-sizing: border-box;
  min-height: 100vh;
  max-width: 90rem;
  border: solid 1px var(--app-color-beige--dark);
  margin: auto;
}

.v--slug__header {
  margin-left: auto;
  margin-right: auto;
  width: calc(100% / 12 * 10);
}


.v--slug__title {
  margin: 5rem 0 0;
  max-width: none;
}

.v--slug__wrap {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.v--slug__wrap__video {
  margin-top: 5rem;
  margin-bottom: 10rem;
  display: block;
  width: calc(100% / 12 * 10);
  border-radius: 2rem;
  box-shadow: 0 0 10px 0 var(--app-color-red);
}

.v--slug__wrap__loading-msg {
  margin-top: 5rem;
  margin-bottom: 10rem;
  width: calc(100% / 12 * 10);
  display: flex;
  align-items: center;
  justify-content: center;
  aspect-ratio: 16/9;
  background: rgba(0, 0, 0, .05);
  border-radius: 2rem;
}
</style>
