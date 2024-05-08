<script setup lang="ts">
import { ref } from 'vue'
import { Button } from '@/components/ui/button'
import { Card, CardHeader, CardContent } from '@/components/ui/card'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>

  <Card>
    <CardHeader class="flex">
      <div class="flex space-x-2">
        <Button @click="count++">count is {{ count }}</Button>
        <Button variant="destructive" @click="count++">count is {{ count }}</Button>
        <Button variant="ghost" @click="count++">count is {{ count }}</Button>
        <Button variant="link" @click="count++">count is {{ count }}</Button>
        <Button variant="outline" @click="count++">count is {{ count }}</Button>
      </div>
    </CardHeader>
    <CardContent>
      <p>
        Edit
        <code>components/HelloWorld.vue</code> to test HMR
      </p>
    </CardContent>
  </Card>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
