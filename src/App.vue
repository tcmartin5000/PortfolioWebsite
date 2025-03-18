<template>

  <header>
    <PageHeader />
  </header>

  <main ref="main-body" class="main-body">
    <Base :parent-height="mainBodyRef != null ? mainBodyRef!.clientHeight : 100" />
  </main>

</template>

<script setup lang="ts">
import { useTemplateRef } from 'vue';
import Base from './components/Base.vue'
import PageHeader from './components/PageHeader.vue'

const mainBodyRef = useTemplateRef('main-body')

</script>

<style scoped>
header {
  line-height: 1.5;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-right: calc(var(--section-gap) / 2);
    position: sticky;
    height: 100vh;
  }

  .main-body {
    display: flex;
    justify-content: start;
    align-items: start;
    height: 100vh;
    overflow-y: scroll;
    padding-left: 10px;
    padding-right: 10px;
  }
}
</style>
