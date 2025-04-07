<template>
    <main
        class="v-documents-slug"
    >
      <template v-if="documentDate">
        <template v-for="n of documentDate.page_number">
          <img :src="`/web/${slug}/image_${String(n - 1).padStart(5, '0')}.jpg`"/>
        </template>
      </template>
    </main>
</template>





<script setup lang="ts">

const documentDate: Ref<{
    'page_number': number
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

img {
  display: block;
  width: 100%;
  max-height: 95vh;
  object-fit: contain;
}
</style>
