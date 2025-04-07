<template>
    <section
        class="v-app-video"
    >
      <div class="v-app-video__wrap">
        <template v-if="video_id">
          <video class="v-app-video__wrap__video"
                 playsinline
                 controls
                 :src="`https://nextcloud.superhangar.cc/s/${video_id}/download/index.mp4`"
          />
        </template>
        <template v-else>
          <div class="v-app-video__wrap__loading-msg">
            récupération de la vidéo :)
          </div>
        </template>
      </div>
    </section>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

defineProps<{
    video_id?: string
}>()
</script>





<style lang="scss" scoped >
.v-app-video__wrap {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.v-app-video__wrap__video {
  display: block;
  width: 100%;
  border-radius: 1rem;
}

.v-app-video__wrap__loading-msg {
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
