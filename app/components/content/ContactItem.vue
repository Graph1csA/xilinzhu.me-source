<script setup>
defineProps(['icon', 'url'])
</script>

<template>
    <a :href="url" class="inline-flex items-center mr-4">
        <img class="w-6 dark:invert mr-2" :src="`/assets/img/icons/${icon}.svg`" alt="" />
        <slot/>
    </a>
</template>
