<template>
    <Transition name="drop" appear>
        <div class="project-with-description-class" v-if="visible">
            <h2>{{ props.projectContents.title }}</h2>
            <p>{{ props.projectContents.content }}</p>
            <div class="pwd-links-class">
                <a v-if="props.projectContents.link != null" :href="props.projectContents.link" class="pwd-link-item-class">View content/demo</a>
                <a v-if="props.projectContents.sourceLink != null" :href="props.projectContents.sourceLink" class="pwd-link-item-class">View source
                    code</a>
            </div>
        </div>
    </Transition>
</template>

<script setup lang="ts">
import type ProjectContents from '@/types/ProjectContents';
import { nextTick, onMounted, ref, type Ref } from 'vue';

type Props = {
    projectContents: ProjectContents,
    msDelay: number
}
const props = defineProps<Props>()
let visible: Ref<boolean> = ref(false);
onMounted(() => {
    return new Promise((resolve) => setTimeout(resolve, props.msDelay)).then(() => visible.value = true)
})
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

.drop-enter-from {
    opacity: 0;
    transform: translateY(-100px);
}

.drop-enter-to {
    opacity: 1;
    transform: translateY(0px);
}

.drop-enter-active {
    transition: all 2s ease;
}
</style>