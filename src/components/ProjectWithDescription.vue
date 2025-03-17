<template>
    <h2>{{ props.title }}</h2>
    <p>{{ props.content }}</p>
    <a :href="props.link">Link to project</a>
    <a :href="props.sourceLink">Link to source code</a>
</template>

<script setup lang="ts">
import type ProjectContents from '@/types/ProjectContents';
const props = defineProps<ProjectContents>()
</script>

<style></style>