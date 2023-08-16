<script setup lang="ts">
import * as PIXI from 'pixi.js'
import { onMounted, ref } from 'vue'

const containerRef = ref<HTMLElement | null>(null)

onMounted(() => {
  const app = new PIXI.Application({ resizeTo: window })
  containerRef.value?.appendChild(app.view as HTMLCanvasElement)
})
</script>

<template>
  <div ref="containerRef"></div>
</template>

<style scoped></style>
