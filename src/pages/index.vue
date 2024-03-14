<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: 'IndexPage',
})

const name = ref('')
</script>

<template>
  <div>
    <!-- TestC defineSlots use vue-macros Short Syntax -->
    <TestC :id="1" :name="name">
      <template #event="{ row, index }">
        {{ row }}-{{ index }}
      </template>
    </TestC>

    <!-- TestD defineSlots use vue-macros Full Syntax (Official Version) -->
    <TestD>
      <template #default="{ msg }">
        {{ msg }}
      </template>

      <template #event="{ row, index }">
        {{ row }}-{{ index }}
      </template>
    </TestD>
  </div>
</template>
