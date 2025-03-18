<template>
    <div class="project-with-description-class">
        <h2>{{ props.title }}</h2>
        <p>{{ props.content }}</p>
        <div class="pwd-links-class">
        <a v-if="props.link != null" :href="props.link" class="pwd-link-item-class">View content/demo</a>
        <a v-if="props.sourceLink != null" :href="props.sourceLink" class="pwd-link-item-class">View source code</a>
        </div> 
    </div>
</template>

<script setup lang="ts">
import type ProjectContents from '@/types/ProjectContents';
const props = defineProps<ProjectContents>()
</script>

<style scoped>
.project-with-description-class {
    background: #242;
    margin: 25px auto;
    padding: 10px 10px;
    border-radius: 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    gap: 10px;
}

.pwd-links-class {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    width: 100%;
}
</style>