<template>
<p>{{ props.textContent }}</p>
</template>

<script setup lang="ts">
    const props = defineProps<{
        textContent?: string
    }>()
</script>

<style>

</style>