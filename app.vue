<template>
  <div class="nuxt-app">

    <div class="nuxt-app__content">
      <NuxtPage/>
    </div>

    <div class="nuxt-app__bg">

      <svg class="nuxt-app__bg__icon"
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

      <svg class="nuxt-app__bg__icon"
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

  </div>
</template>

<style lang="scss" scoped>
.nuxt-app__content {
  position: relative;
  z-index: 10;
}

.nuxt-app__bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.nuxt-app__bg__icon {
  position: absolute;
  display: block;
  height: auto;

  &:nth-child(1) {
    top:  0;
    left: 50%;
    width: 50%;
    transform:
            translate( calc(-50% - 36%), calc( -50% ))
            scale(1.5);
  }

  &:nth-child(2) {
    bottom:  0;
    left: 50%;
    width: 50%;
    transform:
        translate( calc(50%), 50%)
        scale(.65);
    ;
  }
}
</style>
<script setup lang="ts">
</script>
