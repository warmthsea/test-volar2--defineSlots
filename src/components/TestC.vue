<script lang="ts" setup>
defineProps<{
  name: string
  id: number
}>()

defineSlots<{
  event: {
    row: string
    index: number
  }
}>()
</script>

<template>
  <div>
    <p>my name is : {{ name }}</p>
    <p v-for="i in 10" :key="i">
      <slot name="event" :row="`${i}`" :index="i" />
    </p>
  </div>
</template>
