<template>
    <main class="v-documents-slug"
    >
      <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px"
           @click="useRouter().go(-1)"
      >
        <path d="m336-280 144-144 144 144 56-56-144-144 144-144-56-56-144 144-144-144-56 56 144 144-144 144 56 56ZM480-80q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-80q134 0 227-93t93-227q0-134-93-227t-227-93q-134 0-227 93t-93 227q0 134 93 227t227 93Zm0-320Z"/>
      </svg>
      <template v-if="documentDate">
        <template v-for="n of documentDate.page_number">
          <img :src="`/web/${slug}/image_${String(n - 1).padStart(5, '0')}.jpg`"/>
        </template>
      </template>

      <a class="app-button v-documents-slug__download"
         v-if="documentDate?.pdf_link"
         :href="documentDate.pdf_link"
         target="_blank"
      >version PDF</a>
    </main>
</template>





<script setup lang="ts">

const documentDate: Ref<{
    page_number: number
    pdf_link?: string
} | null> = ref(null)

const slug = useRouter().currentRoute.value.params.slug

onMounted(async () => {

    documentDate.value = await (await fetch(`/web/${slug}/data.json`)).json()
})
</script>





<style lang="scss" scoped >
.v-documents-slug {
  min-height: 100vh;
  background: black;
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  padding-top: 1rem;
  padding-bottom: 1rem;
}

svg {
  display: block;
  position: fixed;
  fill: var(--app-color-beige--dark);
  top: var(--app-gutter);
  right: var(--app-gutter);
  width:  3rem;
  height: 3rem;
  user-select: none;
  cursor: pointer;
}

img {
  display: block;
  width: 100%;
  max-height: 95vh;
  object-fit: contain;
}

.v-documents-slug__download {
  position: fixed;
  right: var(--app-gutter);
  bottom: var(--app-gutter);
  background: white;
}
</style>
