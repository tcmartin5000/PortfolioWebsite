<template>
    <div class="project-with-description-class">
    <h2>{{ props.title }}</h2>
    <p>{{ props.content }}</p>
    <a v-if="props.link != null" :href="props.link">Link to project</a>
    <a v-if="props.sourceLink != null" :href="props.sourceLink">Link to source code</a>
    </div>
</template>

<script setup lang="ts">
import type ProjectContents from '@/types/ProjectContents';
const props = defineProps<ProjectContents>()
</script>

<style>
.project-with-description-class {
    background: #242;
    margin: 25px auto;
    padding: 10px 10px;
    border-radius: 15px;
    display: flex;
    align-items: bottom baseline;
    justify-content: space-between;
}
</style>