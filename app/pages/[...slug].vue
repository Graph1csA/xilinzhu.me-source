<script setup lang="ts">
const route = useRoute()
const { data: page } = await useAsyncData(
  route.path,
  () => {
  return queryCollection('page')
    .path(route.path)
    .first()
},
{ watch: [() => route.path] }  // ← Watch for route changes
)
</script>

<template>
    <Navigator class="font-sans" />

    <article class="pb-16 min-h-[100vh]
                    [&_header]:md:max-w-[140%] [&_header]:md:mx-[-20%]
                    [&_pre]:md:text-xs
                    font-serif"
        :class="page!.disableFancyImage ? '' : '[&_p_img]:md:max-w-[140%] [&_p_img]:md:mx-[-20%]'">

        <ContentRenderer :value="page" class="prose dark:prose-invert mx-auto p-4 md:p-0 md:text-lg [&_h1]:mt-12" />

    </article>

    <Footer></Footer>
</template>
