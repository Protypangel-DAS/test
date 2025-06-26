<script setup lang="ts">
import Button from '@alif/storybook/src/ui/Button/Button.vue'
import { ref } from 'vue'

const count = ref<number>(0)

const handleClick = () => {
  count.value++
}
</script>

<template>
  <Button 
    :label="`Click me ${count}`" 
    @click="handleClick" 
    :primary="count % 2 === 0"
    />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
