<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: 'IndexPage',
})

const name = ref('')
</script>

<template>
  <div>
    <TestC :id="('1' as never)" :name="name">
      <template #event="{ row, index }">
        {{ row }}-{{ index }}
      </template>
    </TestC>
  </div>
</template>
